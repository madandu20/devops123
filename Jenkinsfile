pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo "Build stage running..."
            }
        }

        stage('Parallel Tests') {
            when {
                branch 'master'   // ✅ Run this entire parallel block only on master
            }
            parallel {

                stage('Test1') {
                    steps {
                        echo "Running Test1 in parallel on master branch..."
                    }
                }

                stage('Test2') {
                    steps {
                        echo "Running Test2 in parallel on master branch..."
                    }
                }

            }
        }

    }
}
