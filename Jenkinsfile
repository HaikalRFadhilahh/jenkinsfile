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
                    sh "rm -rf .env"
                    script {
                        params.each {param -> 
                            echo "${param.key.trim()}=${param.value.trim()}"
                            sh "echo '${param.key.trim()}=${param.value.trim()}' >> .env"
                        }
                    }
                }
            }
        }
    }
}