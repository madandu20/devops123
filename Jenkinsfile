pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Build stage running..."
            }
        }

        stage('Test1') {
            when {
                branch 'main'     // ✔ Run this stage only on main
            }
            steps {
                echo "Running Test1 only on main branch..."
            }
        }

        stage('Test2') {
            when {
                branch 'main'     // ✔ Run this stage only on main
            }
            steps {
                echo "Running Test2 only on main branch..."
            }
        }
    }
}
