pipeline {
    agent any

    parameters {

        // 1. String parameter
        string(
            name: 'Name',
            defaultValue: 'Kailash',
            description: 'Enter your name'
        )

        // 2. Choice parameter
        choice(
            name: 'Environment',
            choices: ['Development', 'Testing', 'Production'],
            description: 'Select the environment'
        )

        // 3. Boolean parameter
        booleanParam(
            name: 'Deploy',
            defaultValue: false,
            description: 'Do you want to deploy?'
        )
    }

    stages {

        stage('Print Parameters') {
            steps {
                echo "Name: ${params.Name}"
                echo "Selected Environment: ${params.Environment}"
                echo "Deploy: ${params.Deploy}"
            }
        }

        stage('Check Environment') {
            steps {
                script {

                    if (params.Environment == 'Development') {
                        echo "You selected Development environment"

                    } else if (params.Environment == 'Testing') {
                        echo "You selected Testing environment"

                    } else if (params.Environment == 'Production') {
                        echo "You selected Production environment"
                    }
                }
            }
        }

        stage('Deployment') {
            steps {
                script {

                    if (params.Deploy) {
                        echo "Deployment started"
                        echo "Deploying to ${params.Environment}"
                    } else {
                        echo "Deployment skipped"
                    }
                }
            }
        }
    }
}
