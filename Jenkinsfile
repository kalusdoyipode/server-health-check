pipeline {
    agent any

    parameters {
        string(name: 'Name', defaultValue: 'Rama', description: 'Enter your name')
        string(name: 'Age', defaultValue: '23', description: 'Enter your age')
        string(name: 'Marks', defaultValue: '50', description: 'Enter your marks')
    }

    stages {
        stage('Print') {
            steps {
                echo "Hello ${params.Name}"
                echo "Age: ${params.Age}"
                echo "Marks: ${params.Marks}"
            }
        }
    }
}
