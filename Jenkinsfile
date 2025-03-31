pipeline {
    agent any

    environment {
        SUDO_PASS = credentials('jenkins-sudo-password')
    }

    stages {
        stage('Prepare') {
            steps {
                echo 'Installing Node.js v22...'
                sh '''
                    echo "$SUDO_PASS" | sudo -S curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -
                    echo "$SUDO_PASS" | sudo -S apt-get install -y nodejs
                '''
            }
        }

        stage('Build') {
            steps {
                echo 'Showing npm version'
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
