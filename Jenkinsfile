// Declerative way
pipeline {
    agent any 
    stages {
        stage ('init') {
            steps {
                sh "terraform init" // refresh //plan //apply //destroy 
            }
        }
        stage ('Planning') {
            steps {
                sh "terraform plan"
            }
        }
    }
}