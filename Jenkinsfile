pipeline {
    agent any
    
    stages {
        stage('Clone') {
            steps {
                echo 'Cloning...'
            }
        }
        
        stage('Build') {
            steps {
                echo 'Building......'
            }
        }       
        
        stage('Parallel Stage') {
            parallel {
            	stage('Test') {
		            steps {
		                echo 'Running in Parallel  - Testing......'
		            }
        		}
                stage('Code Review') {
                    steps {
                        echo 'Running tasks in parallel - code review'
                    }
                }
                stage('Nexus Upload') {
                    steps {
                        echo 'Running tasks in parallel - nexus upload'
                    }
                }
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}
