pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Build stage running..."
                // put your build commands here
            }
        }

        stage('Test1') {
            when {
                branch 'master'    // run only when the checkout branch is exactly "master"
            }
            steps {
                echo "Running Test1 only on master branch..."
                // run Test1 commands here
            }
        }

        stage('Test2') {
            when {
                branch 'master'
            }
            steps {
                echo "Running Test2 only on master branch..."
                // run Test2 commands here
            }
        }
    }
}
