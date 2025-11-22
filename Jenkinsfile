pipeline {
    agent any

    parameters {
        choice(
            name: 'STAGE_NAME',
            choices: ['Build', 'Test1', 'Test2'],
            description: 'Select which stage to run'
        )
    }

    stages {

        stage('Build') {
            when {
                expression { params.STAGE_NAME == 'Build' }
            }
            steps {
                echo "Running Build stage..."
            }
        }

        stage('Test1') {
            when {
                expression { params.STAGE_NAME == 'Test1' }
            }
            steps {
                echo "Running Test1 stage..."
            }
        }

        stage('Test2') {
            when {
                expression { params.STAGE_NAME == 'Test2' }
            }
            steps {
                echo "Running Test2 stage..."
            }
        }

    }
}
