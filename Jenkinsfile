pipeline {
    stage('Four') {
                parallel {
                    stage('Unit Testing') {
                        steps {
                            echo 'Running the unit Testing!'
                        }
                    }
                    stage('Integration Testing') {
                        
                        steps {
                            echo 'Running the Integration Testing!'
                        }
                    }
                }
            }
}