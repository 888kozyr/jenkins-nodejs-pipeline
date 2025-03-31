pipeline {
    agent any

    stages {
        stage('Prepare') {
            steps {
                echo 'Installing Node.js v22...'
                sh '''
                    sudo curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -
                    sudo apt-get install -y nodejs
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
