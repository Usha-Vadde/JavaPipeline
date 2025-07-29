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
        stage('Package JAR') {
            steps {
                bat 'jar cfm factorial.jar manifest.txt Factorial.class'
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
