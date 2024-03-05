pipeline {
    agent any
    stages {
        stage('Display Info') {
            steps {
                script {
                    echo "Jenkins URL: ${env.JENKINS_URL}"
                    echo "Build ID: ${env.BUILD_ID}"
                }
            }
        }
        // Add more stages as needed
    }
}
