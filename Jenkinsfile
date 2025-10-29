pipeline {
    agent any

    parameters {
        choice(
            name: 'ACTION',
            choices: ['apply', 'destroy'],
            description: 'Select the action to perform'
        )
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/tribhuwanpandey/Eks-cluster-deployment.git'
            }
        }

        stage('Terraform Init') {
            steps {
                sh 'terraform init -reconfigure'
            }
        }

        stage('Plan') {
            steps {
                sh 'terraform plan'
            }
        }

        stage('Action') {
            steps {
                script {
                    switch (params.ACTION) {
                        case 'apply':
                            echo 'Executing Apply...'
                            sh 'terraform apply --auto-approve'
                            break
                        case 'destroy':
                            echo 'Executing Destroy...'
                            sh 'terraform destroy --auto-approve'
                            break
                        default:
                            error 'Unknown action'
                    }
                }
            }
        }
    }
}
