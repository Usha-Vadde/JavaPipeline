pipeline {
    agent any

    stages {
        
        stage('Compile') {
            steps {
                bat 'javac Factorial.java TestFactorial.java'
            }
        }

        stage('Test') {
            steps {
                bat 'java TestFactorial'
            }
        }

        
    }

    post {
        success {
            echo 'Factorial Java program built and tested successfully!'
        }
        failure {
            echo 'Build or test failed!'
        }
    }
}
