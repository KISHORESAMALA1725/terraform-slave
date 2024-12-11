pipeline {
    agent {
        label 'terraform-slave'
    }
    parameters {
        string (name: 'Please enter your name', defaultValue: 'KISHORE', description: '#####')
        choices (name: 'Please select one option', choices: ["terraform init"])
    }
}
