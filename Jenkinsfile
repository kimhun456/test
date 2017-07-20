pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                sh 'echo "TEST!"'
            }
        }
        stage('Build') {
            steps {
                sh 'echo "BUILD!"'
            }
        }
    }
    post {
        always {
            echo 'This will always run'
            deleteDir()
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
