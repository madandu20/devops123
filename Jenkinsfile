pipeline {
    agent any

    stages {

        stage('A') {
            steps {
                script {
                    echo "Running Stage A..."
                    // Add your real commands here
                    // Example command that may fail:
                    // sh 'exit 1'
                }
            }
        }

        stage('B') {
            when {
                expression { currentBuild.result == null || currentBuild.result == 'SUCCESS' }
            }
            steps {
                echo "Stage A succeeded → Running Stage B"
            }
        }

        stage('C') {
            when {
                expression { currentBuild.result == 'FAILURE' }
            }
            steps {
                echo "Stage A failed → Running Stage C"
            }
        }
    }

    post {
        failure {
            script {
                currentBuild.result = 'FAILURE'
            }
        }
    }
}
