pipeline {
    agent any

    stages {

        stage('Install Dependencies') {
            steps {
                    sh "npm install"
                }
        }

        stage('Build') {
            steps {
                sh "npm run build"
            }
        }

        stage('Deploy') {
            steps {
                
                    sh "scp -r build/* ubuntu@54.197.41.224:/var/www/html/"
                }
            }
        }
}

    
