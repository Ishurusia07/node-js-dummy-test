pipeline {
    environment {
    env = 'dev'
  }
    agent any
    options {
        skipStagesAfterUnstable()
    }
        stage('NPM install') { 
            steps { 
                sh 'ssh root@192.168.1.8 "cd cd /home/ishu/test.com && npm install"'
            }
        }
        stage('Reload PM2') { 
            steps { 
                sh 'ssh root@192.168.1.8 "cd /home/ishu/test.com && pm2 reload 0"'
            }
       }
  }
