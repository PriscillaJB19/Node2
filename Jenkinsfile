@Library("shared-library")_
pipeline {
    agent any
    
    tools{
        nodejs 'nodejs'
    }
    
    environment {
        REGISTRY = 'priscillajb/node-app'
    }
    
    stages{

		stage('Install'){
            steps{
				Dependencies();
            }
    }
}
}