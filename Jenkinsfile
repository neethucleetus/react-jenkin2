pipeline {
    agent any 
   
   stages {
        stage('Build') {
            steps {
                bat 'npm install'
            }
        }
       stage('Test') {
                    steps {
                        bat 'npm test'
                    }
       }
       stage('Deliver') {
                            steps {
                               bat 'npm run build'
                            }
                        }
   }
    
}
