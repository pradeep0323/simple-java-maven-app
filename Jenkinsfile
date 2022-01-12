pipeline {
    agent {
        label 'agent1'
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
    post {
        always {
            echo "send mail to all ..." 
        }
    }
}
