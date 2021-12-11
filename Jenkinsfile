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
                            docker {
                                reuseNode false
                                image 'node:alpine'
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