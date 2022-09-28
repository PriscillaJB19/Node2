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
				Dependencies()
            }
    }

    	stage('Build'){
            steps{
                Build(registry:REGISTRY,buildNumber:"${BUILD_NUMBER}")
            }
    }
}
}