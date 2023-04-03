pipeline{
    agent any
    stages{
        // Install python packages *
        stage('Ls file'){
            steps{
                sh 'ls -l'
            }
        }
        stage('Python Requirements'){
            steps{
                sh 'python -m venv env'
                sh 'source /env/bin/activate'
                sh 'pip install -r requirements.txt'
            }
        }
        // Run the tests
        stage('Run Pytest'){
            steps{
                sh 'source /env/bin/activate'
                sh 'cd env && pytest -v'
            }
        }
    }
}
