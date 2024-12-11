pipeline {
    agent {
        label 'terraform-slave'
    }
    parameters {
        string (name: 'Please enter your name', defaultValue: 'KISHORE', description: '#####')
        choices (name: 'Please select one option', choices: ["init","validate"], description: "this is terraform")
    }
    stages {
        stage ('this is terraform init stage') {
            when {
                expression {
                    params.choices == "init"
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
