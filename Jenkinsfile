@Library("shared-library")_
pipeline {
    agent any
    
    tools{
        nodejs 'nodejs'
    }
    
    environment {
        REGISTRY = 'priscillajb/nodeapp'
    }
    
    stages{

		stage('Install'){
            steps{
				Dependencies()
            }
    }
}
}