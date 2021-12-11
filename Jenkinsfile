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
            stage('three') {
                steps {
                    input('Input to proceed?');
                }
                when { branch 'maindsd' }
                    
            }
        }
}