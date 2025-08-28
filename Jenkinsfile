
pipeline{
    agent any
    options{
        buildDiscarder(logRotator(numToKeepStr: '3'))
    }
    stages {
        stage ('Build'){
            steps {
                    echo "***hi Build****"
                }
            }
        stage ('Scans') {
            parallel {
                stage ('stage-1') {
                    steps {
                        sleep 10
                    }
                } 
                stage ('stage-2'){
                    steps {
                        sleep 10
                    }
                }          
            }           
        } 
        stage ('prod'){
            input {
                message "ready to deploy?"
                ok 'yes'
                submitter 'admin needs to approve this'
            }
            steps {
                    echo "***hi Build****"
                }
            }             
        }
    }
