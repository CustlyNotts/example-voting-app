pipeline {
    
    agent any

    tools {
	maven 'Maven 3.8.6'
	}
    
    stages {
        stage('onne') {
            steps {
                echo 'Compiling worker app'
                dir('worker') {
		sh 'mvn compile'
		}
            }
        }
        
        stage('two') {
            steps {
                echo 'Running Unit tests on worker app'
                sleep 9
            }
            
        }
            stage('three') {
            steps {
                echo 'Packaging worker app'
                sleep 5
            }
            
        }

    }
    
    post {
        always {
            echo 'Build pipeline for worker app is completed...'
        }
    }
}
