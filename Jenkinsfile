@Library("shared-library")_
pipeline {
    agent any
    
    tools{
        nodejs 'nodejs'
    }
    
    environment {
        PROJECT_ROOT = 'package.json'
        REGISTRY = 'priscillajb/nodeapp'
    }
    
    stages{

		stage('Install'){
            steps{
                echo "${PROJECT_ROOT}"
				Dependencies(project_root:PROJECT_ROOT)
            }
    }
}
}