pipeline {
    agent any
    
    environment {
        JOB_NAME_PATH = "${env.JOB_NAME.replace('/', '_')}"
        WORKSPACE_LOCATION = "/var/www/html/jenkins-workspace/${JOB_NAME_PATH}"
    }

    stages {
        stage ('Setting Workspace Location') {
            steps {
                dir(WORKSPACE_LOCATION){
                    sh 'echo "Change Github Clone With Custom Workspace"'
                    checkout scm
                }
            }
        }
        stage  ('Setting Environment Variabel'){
            steps {
                dir(WORKSPACE_LOCATION) {
                    script {
                        params.each {param -> 
                            sh 'echo "${param.key.trim()}=${param.value.trim()}"'
                        }
                    }
                }
            }
        }
    }
}