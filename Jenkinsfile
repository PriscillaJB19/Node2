@Library("shared-library")_
pipeline {
    agent any
    
    tools{
        nodejs 'nodejs'
    }
    
    environment {
        PROJECT_ROOT = './'
        REGISTRY = 'priscillajb/node-app'
    }
    
    stages{

		stage('Install'){
            steps{
                echo "${PROJECT_ROOT}"
				Dependencies(project_root:PROJECT_ROOT)
            }
    }

    	stage('Build'){
            steps{
                Build(project_root:PROJECT_ROOT,registry:REGISTRY,buildNumber:"${BUILD_NUMBER}")
            }
    }
}
}