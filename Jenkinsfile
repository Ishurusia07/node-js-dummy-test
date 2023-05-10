pipeline {
    environment {
        env = 'dev'
    }
    agent any
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('NPM install') {
            steps {
                sh 'cd /home/ishu/test.com && sudo npm install'
            }
        }
        stage('Reload PM2') {
            steps {
                sh 'cd /home/ishu/test.com && sudo pm2 reload 0'
            }
        }
    }
}
