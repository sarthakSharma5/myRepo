pipeline {
    agents any
    
    stages {
        stage('Dev Env') { 
            steps { 
                sh "echo dev" 
            }
        }
        stage('Test'){
            steps {
                sh "echo test"
                timeout(time: 2, unit: 'DAYS'){
                    input message: 'waiting for approval:'
                }
            }
        }
        stage('Prod') {
            steps {
                sh "echo deploy"
            }
        }
    }
}
