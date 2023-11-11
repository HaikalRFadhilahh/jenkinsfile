pipeline{
    agent 
    
    stages {
        stage ('Setting Workspace Location') {
            steps {
                dir('/var/www/html/jenkins-workspace'){
                    sh 'echo "Change Github Clone With Custom Workspace"'
                }
            }
        }
        stage ('Setting Environment') {
            steps {
                echo 'Testing Jenkinsfile Works!'
            }
        }
    }
}