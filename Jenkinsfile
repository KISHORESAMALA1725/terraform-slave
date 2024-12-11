pipeline {
    agent {
        label 'terraform-slave'
    }
    parameters {
        string (name: 'USERNAME', defaultValue: 'KISHORE', description: 'Please enter your name')
        choice (name: 'terraform', choices: ["init","validate","apply","destroy"], description: "this is terraform")
    }
    stages {
        stage ('this is terraform init stage') {
            when {
                expression {
                    params.terraform == "init"
                }
            }
            steps {
                script {
                    sh "terraform init"
                }
            }
        }
        stage ('This is Terraform validate: stage') {
            when {
                expression {
                    params.terraform == "validate"
                }
            }
            steps {
                script {
                    sh "terraform validate"
                }
            }
        }
        stage ('This is terraform apply') {
            when {
                expression {
                    params.terraform == "apply"
                }
            }
            steps {
                script {
                    sh "terraform apply -y"
                }
            }
        }
        stage ('Terraform destory') {
            steps {
                script {
                    sh "terraform destroy --auto-approve"
                }
            }
        }
    }
}
