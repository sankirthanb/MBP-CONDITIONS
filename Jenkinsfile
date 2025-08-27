pipeline{
    agent any
    stages {
            stage ('build') {
                steps {
                    echo "*** this is build stage ***"
                }
            }
            stage ('build-art') {
                steps {
                    echo "*** this is build stage ***"
                }
            }
            stage ('sonar') {
                steps {
                    echo "*** this is sonar stage ***"
                }
            }
            stage ('nexus') {
                steps {
                    echo "*** this is nexus stage ***"
                }
            }
            stage ('docker') {
                steps {
                    echo "*** this is docker stage ***"
                }
            }
            stage ('dcker push') {
                steps {
                    echo "*** this is docker-push stage ***"
                }
            }
            stage ('dev') {
                steps {
                    echo "*** this is dev stage ***"
                }
            }
            stage ('test') {
                steps {
                    echo "*** this is qa stage ***"
                }
            }
            stage ('qa') {
                   when {
                       branch 'release/*'
                   }   
                steps {
                    echo "*** this is qa stage ***"
                }
            }  
             stage ('prod') {
                   when {
                       tag pattern: "v\\d{1,2}.\\d{1,2}\\.\\d{1,2}", comparator: "REGEXP" 
                   }
                steps {
                    echo "*** this is prod stage ***"
                }
            }            
                   
        }
    }
