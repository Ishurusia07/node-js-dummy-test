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
               'cd /home/ishu/test.com && sudo npm install'
            }
        }
        stage('Reload PM2') {
            steps {
               'cd /home/ishu/test.com && sudo pm2 reload 0'
            }
        }
    }
}
