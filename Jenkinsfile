pipeline {
    agent {
        label 'terraform-slave'
    }
    stages {
        stage ('This is terraform-slave test') {
            steps {
                script {
                    sh "hostname -a"
                    sh "hostname"
                    echo "Hostname"
                }
            }
        }
    }
}
