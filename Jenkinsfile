pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/anxhela2001/CSY3056'
            }
        }

        stage('Build') {
            steps {
                bat '''
                echo "== Starting Build =="
                cd "%WORKSPACE%"
                mkdir build // Ensures build folder exists
                npm install
                echo "== Build Completed! =="
                '''
            }
        }

        stage('Test') {
            steps {
                bat '''
                echo "== Running Tests =="
                cd "%WORKSPACE%"
                npm test
                echo "== Tests Completed! =="
                '''
            }
        }

        stage('Deploy') {
            steps {
                bat '''
                echo "== Deploying Application =="
                echo "== Deploying Successful! =="
                '''
            }
        }
    }
}
