pipeline {
    agent any
        stages
        {
            stage('One') {
                steps {
                    echo 'hi1'
                }
            }
            stage('two') {
                steps {
                    input('Input to proceed?');
                }
            }
            stage('test'){
                when {
                    changeset "*.yaml"
                }
                steps{
                    echo "The file did change in the last commit (SCM checking)"
                }
            }
        }
}