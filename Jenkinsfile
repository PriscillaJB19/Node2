@Library('shared-library')_
pipeline{
    agent any 

    stages{
        stage('docker build'){
            steps{
                script{
                    dockerLib.build(DockerfilePath:"node/dockerfile",
                    DockerImage:"priscillajb/nodeapp-${BUILD_ID}",
                    DockerContext:"node")
                }
            }
        }

    stage('docker push'){
        steps{
            script{
                dockerLib.push(DockerImage:"priscillajb/nodeapp-${BUILD_ID}")
            }
            }
        }
    }
}