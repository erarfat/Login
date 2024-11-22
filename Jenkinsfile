pipeline {
    agent any
    parameters {
        choice(name: 'ACTION', choices: ['start', 'stop'])
    }
    stages {
        stage('Docker Action') {
            steps {
                script {
                    if (params.ACTION == 'start') {
                        echo "Starting Docker containers..."
                        sh 'docker-compose up -d'
                        
                    } else if (params.ACTION == 'stop') {
                        echo "Stopping Docker containers..."
                        sh 'docker-compose down'
                    }
                }
            }
        }
    }
}


