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
        stage('sonar analysis') {
            steps {
                sh 'mvn sonar:sonar'
            }
        }
    }
    post {
        always {
            echo "send mail to all ..." 
        }
    }
}
