pipeline{
    environment {
        deploy_to = "prod"
    }
    agent any {
        stages {
            stage ('main') {
                when {
                    enivornment name = 'deploy_to', value: 'prod'
                }
                steps {
                    echo "*** this is prod stage ***"
                }
            }
        }
    }
}


###3


pipeline{
    agent any
    stages {
            stage ('main') {
                when {
                    expression {BRANCH_NAME ==~ /(production | staging )/}
                }
                steps {
                    echo "*** this is prod stage ***"
                }
            }
        }
    }


#### anyof condition


pipeline{
    agent any
    environment {
        deploy_to = "somthing"
    }
    stages {
            stage ('main') {
                when { 
                    anyOf { ### any of these is true, it will work
                    expression {BRANCH_NAME ==~ /(production | staging )/}
                    enivornment name = 'deploy_to', value: 'prod'    
                        
                    }    
                }
                steps {
                    echo "*** this is prod stage ***"
                }
            }
        }
    }


## all of 


pipeline{
    agent any
    environment {
        deploy_to = "somthing"
    }
    stages {
            stage ('main') {
                when { 
                    allOf { ### all of these is true, it will work
                    expression {BRANCH_NAME ==~ /(production | staging )/}
                    enivornment name = 'deploy_to', value: 'prod'    
                        
                    }    
                }
                steps {
                    echo "*** this is prod stage ***"
                }
            }
        }
    }


pipeline{
    agent any
    stages {
            stage ('build) {
                steps {
                    echo "*** this is build stage ***"
                }
            }
            stage ('build) {
                steps {
                    echo "*** this is build stage ***"
                }
            }
            stage ('sonar) {
                steps {
                    echo "*** this is sonar stage ***"
                }
            }
            stage ('nexus) {
                steps {
                    echo "*** this is nexus stage ***"
                }
            }
            stage ('docker) {
                steps {
                    echo "*** this is docker stage ***"
                }
            }
            stage ('dcker push ) {
                steps {
                    echo "*** this is docker-push stage ***"
                }
            }
            stage ('dev) {
                steps {
                    echo "*** this is dev stage ***"
                }
            }
            stage ('test) {
                steps {
                    echo "*** this is qa stage ***"
                }
            }
            stage ('qa) {
                   when {
                       branch 'release/*'
                   }
                steps {
                    echo "*** this is qa stage ***"
                }
            }  
             stage ('prod) {
                   when {
                       tag pattern: "v\\d{1,2}.\\d{1,2}\\.\\d{1,2}", comparator: "REGEXP" 
                   }
                steps {
                    echo "*** this is prod stage ***"
                }
            }            
                   
        }
    }


