pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                sh 'echo "Success!"'
            }
            steps{
                sh ' echo "this is second step" '   
            }
        }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previoasdfusly failing but is now successful'
        }
    }
}
