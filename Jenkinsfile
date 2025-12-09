pipeline {
    agent any

    stages {
        stage('A') {
            steps {
                sh 'echo "Stage A"'
            }
        }

        stage('B') {
            steps {
                // If commands inside here fail, the build stays SUCCESS
                catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
                    sh 'exit 1'   // simulate failure
                }
            }
        }

        stage('C') {
            steps {
                sh 'echo "Stage C"'
            }
        }
    }
}
