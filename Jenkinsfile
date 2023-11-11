pipeline {
    agent any
    
    environment {
        JOB_NAME_PATH = "${env.JOB_NAME.replace('/', '_')}"
        WORKSPACE_LOCATION = "/var/www/html/jenkins-workspace/${JOB_NAME_PATH}"
    }

   parameters {
    string(name: 'NAME',defaultValue: 'your name',description: 'Untuk Mencoba Nama Pada Jenkinsfile Build With Paramater')
   }

    stages {
        stage ('Setting Workspace Location') {
            steps {
                // sh 'cd /var/lib/jenkins/workspace/ && rm -rf *'
                dir(WORKSPACE_LOCATION){
                    sh 'echo "Change Github Clone With Custom Workspace"'
                    checkout scm
                }
            }
        }
        stage  ('Setting Environment Variabel'){
            steps {
                dir(WORKSPACE_LOCATION) {
                    echo 'wkwkwk Land'
                    sh 'docker ps'
                    
                    echo "Selamat Pagi ${NAME}"
                }
            }
        }
    }
}