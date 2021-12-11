pipeline {
    agent any
        stages
        {
            stage('One') {
                steps {
                    echo 'Starting...'
                }
            }
            stage('two') {
                steps {
                    //input('Input to proceed?');
                    echo 'hi input'
                }
            }
            stage('test'){
                when {
                    changeset "*.js"
                }                                
                steps{
                    echo "The file did change in the last commit (SCM checking)"
                }
            }
            stage('Four') {
                parallel {
                    stage('Unit Testing') {
                        steps {
                            echo 'Running the unit Testing!'
                        }
                    }
                    stage('Integration Testing') {
                        agent {
                            dockerfile {
                                filename 'Dockerfile'
                                registryUrl 'https://hub.docker.com/repository/docker/munawersheikh/docker-example'
                                registryCredentialsId 'munawersheikh/******'                             
                            }
                        }
                        steps {
                            echo 'Running the Integration Testing!'
                        }
                    }
                }
            }
        }
}