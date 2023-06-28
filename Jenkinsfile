pipeline {
    agent any
    
    stages {
        stage ('Build') {
            steps {
                sh 'mvn install' 
            }
            post {
                success {
                    junit 'target/surefire-reports/*/.xml' 
                }
            }
        }
    }
}
