pipeline {
    agent any
        stages
        {
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
                                registryCredentialsId 'munawer-repo'                             
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