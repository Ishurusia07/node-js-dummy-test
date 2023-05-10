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
              sh 'ssh ishu@192.168.1.8 "cd /home/ishu/test.com && npm install"'
            }
        }
        stage('Reload PM2') {
            steps {
             sh 'ssh ishu@192.168.1.8 "cd /home/ishu/test.com && pm2 reload 0"'
            }
        }
    }
}
