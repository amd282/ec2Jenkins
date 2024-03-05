pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Display Jenkins URL & BUILD_ID') {
            steps {
                script {
                    // Add a condition to trigger only for the 'main' branch
                    if (env.BRANCH_NAME == 'main') {
                        echo "JENKINS_URL: ${env.JENKINS_URL}"
                        echo "BUILD_ID: ${env.BUILD_ID}"
                        echo "BRANCH_NAME: ${env.BRANCH_NAME}"
                        echo "CHANGE_ID: ${env.CHANGE_ID}"
                        echo "CHANGE_URL: ${env.CHANGE_URL}"
                        echo "CHANGE_TITLE: ${env.CHANGE_TITLE}"
                        echo "CHANGE_AUTHOR: ${env.CHANGE_AUTHOR}"
                    } else {
                        echo "Pipeline not triggered for branch: ${env.BRANCH_NAME}"
                    }
                }
            }
        }
    }
}
