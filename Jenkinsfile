pipeline {
    agent any
    
    environment {
        NAMA_JOB = env.JOB_NAME
    }

    stages {
        stage ('Setting Workspace Location') {
            steps {
                dir('/var/www/html/jenkins-workspace/${env.NAMA_JOB}'){
                    sh 'echo "Change Github Clone With Custom Workspace"'
                }
            }
        }
        stage  ('Setting Environment Variabel'){
            steps {
                dir('/var/www/html/jenkins-workspace/${env.NAMA_JOB}') {
                    echo 'wkwkwk Land'
                }
            }
        }
    }
}