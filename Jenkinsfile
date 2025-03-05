pipeline {
    agent any
    stages{
        stage('CodeScan'){
            sh 'trivy --version'
        }
        stage('dockerImageBuild'){
            steps{
                sh 'docker -v'

            }
        }
        stage(dockePush){
            steps{
                sh 'docker ps'
            }
        }

        stage('clone'){
            steps{
                sh 'echo "clone"'
            }
            stage('test'){
                steps{
                    sh 'echo "test"'
                }
            }
            stages('createfile'){
                steps{
                    sh 'touch test-$BUILD_ID'
                }
            }
        }

    }
}
