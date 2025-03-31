pipeline {
    agent any

    stages {
        stage('Prepare') {
            steps {
                echo 'Installing Node.js v22...'
                sh '''
                    curl -fsSL https://deb.nodesource.com/setup_22.x | bash -
                    apt-get install -y nodejs
                '''
            }
        }

        stage('Build') {
            steps {
                sh 'npm --version'
            }
        }

        stage('Test') {
            steps {
                echo "JENKINS_URL is: ${env.JENKINS_URL}"
            }
        }
    }
}
