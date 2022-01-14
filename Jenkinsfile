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
                WithSonarQubeEnv('sonarqube9.2'){
                sh 'mvn sonar:sonar'
                }
            }
        }
    }
    post {
        always {
            echo "send mail to all ..." 
        }
    }
}
