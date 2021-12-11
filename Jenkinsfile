pipeline {
    agent any
        stages{
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
            stage('three') {
                when {
                    not {
                        branch 'main1'
                    }
                }
                steps {
                    echo 'hi23'
                }
                
            }
        }
}