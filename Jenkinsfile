pipeline {
    agent any

    parameters {
        string(
            name: 'Name',
            defaultValue: 'Kailash',
            description: 'Enter your name'
        )

        choice(
            name: 'Environment',
            choices: ['Development', 'Testing', 'Production'],
            description: 'Select environment'
        )

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
                echo "Environment: ${params.Environment}"
                echo "Deploy: ${params.Deploy}"
            }
        }
    }
}
