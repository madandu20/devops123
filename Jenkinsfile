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
                catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE'){
                sh 'exit 1'      // <-- this fails the build now
            }
        }

        stage('C') {
            steps {
                sh 'echo "Stage C"'
            }
        }
    }
}
