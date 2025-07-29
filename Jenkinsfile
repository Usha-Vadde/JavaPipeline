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
        stage('Run') {
            steps {
                bat 'java Factorial'
            }
        }
        
        
    }

    post {
        success {
            echo 'Build, test, run and JAR cretaion successful and artifact is ready!'
        }
        failure {
            echo 'Build or test failed!'
        }
    }
}
