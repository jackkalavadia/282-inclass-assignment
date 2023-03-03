pipeline {
    agent any
       triggers {
        pollSCM "* * * * *"
       }
    stages {
        stage('Build Application') { 
            steps {
                echo '=== Building Petclinic Application ==='
            }
        }
        stage('Test Application') {
            steps {
                echo '=== Testing Petclinic Application ==='
            }
        }
        stage('Build Docker Image') {
            when {
                branch 'main'
            }
            steps {
                echo '=== Building Petclinic Docker Image ==='
            }
        }
        stage('Push Docker Image') {
            when {
                branch 'main'
            }
            steps {
                echo '=== Pushing Petclinic Docker Image ==='
            }
        }
        stage('Remove local images') {
            steps {
                echo '=== Delete the local docker images ==='
            }
        }
    }
}
