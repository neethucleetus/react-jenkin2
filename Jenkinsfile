pipeline {
    agent any
     environment {
            CI = 'true'
        }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
        	    echo "Build"
            }
        }
        stage('Test') {
                    steps {
			        echo "Test"
                        sh './jenkins/scripts/test.sh'
			            echo "Test1"
                    }
                }
                stage('Deliver') {
                            steps {
				                echo "Test2"
                                sh './jenkins/scripts/deliver.sh'
				                echo "Test3"
                                input message: 'Finished using the web site? (Click "Proceed" to continue)'
				                echo "Test4"
                                sh './jenkins/scripts/kill.sh'
				                echo "Test5"
                            }
                        }

    }
}
