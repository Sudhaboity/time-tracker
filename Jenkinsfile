pipeline {
    agent any
    
    tools {
        maven 'local_maven'
    }
    stages{
        stage('Build'){
            steps {
                sh 'mvn clean package'
            }
            post {
                success {
                    echo 'Archiving the artifacts'
                    archiveArtifacts artifacts: '*/web/target/.war'
                }
            }
        }

        stage ('Deployments'){
                    steps {
                       echo 'depploy'
                    }
                }
            }
        }
