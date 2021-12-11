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
                when { branch 'maindsd' }
                        echo 'hi23 mew 1 2'
                    
            }
        }
}