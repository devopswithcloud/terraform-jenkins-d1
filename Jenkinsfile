// Declerative way
pipeline {
    agent any
    parameters {
        choice (
            name: 'action',
            choices: 'no\napply\ndestroy',
            description: "Apply and destroy app1 infrastructure"
        )
    } 
    stages {
        stage ('init') {
            when {
                expression {
                    params.action == 'apply'
                }
            }
            steps {
                sh "terraform init" // refresh //plan //apply //destroy 
            }
        }
        stage ('Plan') {
            when {
                expression {
                    params.action == 'apply'
                }
            }
            steps {
                sh "terraform plan"
            }
        }
        stage ('apply') {
            when {
                expression {
                    params.action == 'apply'
                }
            }
            steps {
                sh "terraform apply --auto-approve"
            }
        }
        stage ('destroy') {
            when {
                expression {
                    params.action == 'destroy'
                }
            }
            steps {
                sh "terraform destroy --auto-approve"
            }
        }
    }
}