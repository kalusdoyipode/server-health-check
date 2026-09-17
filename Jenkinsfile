pipeline {
    agent any

    stages {

        stage('Test') {
            steps {
                script {

                    try {
                        echo "Test started"
                        sh 'exit 1'

                    } catch (Exception e) {
                        echo "Test failed"
                        echo "Handling the error"

                    } finally {
                        echo "Cleanup is always executed"
                    }
                }
            }
        }

        stage('Next Stage') {
            steps {
                echo "Pipeline continues"
            }
        }
    }
}  
