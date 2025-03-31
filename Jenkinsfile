pipeline {
    agent any

    stages {
        stage('Prepare') {
            steps {
                echo 'Installing Node.js v22...'
                sh '''
                    curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -
                    sudo apt-get install -y nodejs
                '''
            }
        }

        stage('Build') {
            steps {
                echo 'Showing npm version (simulate build)'
                sh 'npm --version'
            }
        }

        stage('Test') {
            steps {
                echo "Simulating test... JENKINS_URL is: ${env.JENKINS_URL}"
            }
        }
    }
}
