@Library("shared-library")_
pipeline {
    agent any
    
    tools{
        nodejs 'nodejs'
    }
    
    environment {
        PROJECT_ROOT = 'Jenkinsfile'
        REGISTRY = 'priscillajb/node-app'
    }
    
    stages{

		stage('Install'){
            steps{
                echo "${PROJECT_ROOT}"
				Dependencies(project_root: PROJECT_ROOT)
            }
    }
}
}