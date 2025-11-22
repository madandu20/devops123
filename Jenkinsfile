pipeline {
    agent any

    parameters {
        string(
            name: 'STAGE_TO_RUN',
            defaultValue: 'A',
            description: 'Enter the stage to run (A, B, or C)'
        )
    }

    stages {

        stage('A') {
            when {
                expression { params.STAGE_TO_RUN == 'A' }
            }
            steps {
                echo "Running Stage A ..."
            }
        }

        stage('B') {
            when {
                expression { params.STAGE_TO_RUN == 'B' }
            }
            steps {
                echo "Running Stage B ..."
            }
        }

        stage('C') {
            when {
                expression { params.STAGE_TO_RUN == 'C' }
            }
            steps {
                echo "Running Stage C ..."
            }
        }

    }
}
