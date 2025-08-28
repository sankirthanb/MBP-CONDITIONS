pipeline{
    agent any
    stages {
            stage ('Build'){
                    steps {
                        echo "***hi Build****"
                    }
                }
            parallel {
                stage ('stage-1') {
                    steps {
                        sleep 10
                    }
                } 
            }
                stage ('stage-2'){
                    steps {
                        sleep 10
                    }
                }          
            }
        }
    }
