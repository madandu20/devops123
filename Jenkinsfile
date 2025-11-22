pipeline {
    agent any

    parameters {
        choice(
            name: 'STAGE_TO_RUN',
            choices: ['A', 'B', 'C'],
            description: 'Select the stage to run'
        )
    }

    stages {

        stage('A') {
            when {
                expression { params.STAGE_TO_RUN == 'A' }
            }
            steps {
                echo "Running Stage A..."
            }
        }

        stage('B') {
            when {
                expression { params.STAGE_TO_RUN == 'B' }
            }
            steps {
                echo "Running Stage B..."
            }
        }

        stage('C') {
            when {
                expression { params.STAGE_TO_RUN == 'C' }
            }
            steps {
                echo "Running Stage C..."
            }
        }
    }
}
