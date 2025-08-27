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
