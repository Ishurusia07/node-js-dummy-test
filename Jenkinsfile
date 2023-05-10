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
                sh 'cd /home/ishu/test.com && npm install'
            }
        }
        stage('Reload PM2') {
            steps {
                sh 'cd /home/ishu/test.com && pm2 reload 0'
            }
        }
    }
}
