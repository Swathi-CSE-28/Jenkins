pipeline {
    agent any

    tools {
        jdk 'JDK21'
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Swathi-CSE-28/Jenkins.git'
            }
        }

        stage('Compile') {
            steps {
                bat 'javac SumOfTwoNumbers.java'
            }
        }

        stage('Execute') {
            steps {
                bat 'java SumOfTwoNumbers'
            }
        }
    }

    post {
        success {
            echo 'Program Executed Successfully'
        }
        failure {
            echo 'Program Execution Failed'
        }
        always {
            echo 'Pipeline Completed'
        }
    }
}
