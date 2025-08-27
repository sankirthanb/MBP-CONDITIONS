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

