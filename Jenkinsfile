pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo "Build started"

                catchError(buildResult: 'FAILURE', stageResult: 'FAILURE') {
                    sh 'exit 1'
                }

                echo "Pipeline continues after catchError"
            }
        }

        stage('Test') {
            steps {
                echo "Testing started"
                echo "Testing completed"
            }
        }
    }
}
    
