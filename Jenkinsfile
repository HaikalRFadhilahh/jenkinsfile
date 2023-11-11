pipeline {
    agent any
    
    environment {
        JOB_NAME_PATH = "${env.JOB_NAME.replace('/', '_')}"
        WORKSPACE_LOCATION = "/var/www/html/jenkins-workspace/${JOB_NAME_PATH}"
    }

    stages {
        stage ('Remove Project Old Path') {
            def pathWorkspace = '/var/lib/jenkins/workspace'
            sh 'rm -rd ${pathWorkspace}/*'
        }
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
                }
            }
        }
    }
}