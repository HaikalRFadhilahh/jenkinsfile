pipeline {
    agent any
    
    stages {
        stage ('Setting Workspace Location') {
            steps {
                dir('/var/www/html/jenkins-workspace/belajar-jenkins'){
                    sh 'echo "Change Github Clone With Custom Workspace"'
                }
            }
        }
        stage  ('Setting Environment Variabel'){
            steps {
                dir('/var/www/html/jenkins-workspace/belajar-jenkins') {
                    echo 'wkwkwk Land'
                }
            }
        }
    }
}