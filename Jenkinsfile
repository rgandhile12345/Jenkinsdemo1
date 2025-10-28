pipeline {
    agent any

    environment {
        PYTHON = 'C:\\Users\\Rahul\\AppData\\Local\\Programs\\Python\\Python313\\python.exe'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Setup Python') {
            steps {
                bat "${env.PYTHON} --version"
            }
        }

        stage('Extract') {
            steps {
                bat "${env.PYTHON} extractdata.py"
            }
        }
    }
}