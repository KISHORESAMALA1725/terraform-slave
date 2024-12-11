pipeline {
    agent {
        label 'terraform-slave'
    }
    parameters {
        string (name: 'Please enter your name', defaultValue: 'KISHORE', description: '#####')
        choice (name: 'terraform', choices: ["init","validate"], description: "this is terraform")
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
    }
}
