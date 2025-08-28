pipeline {
    agent any
    parameters{
        string(name: 'change Ticket', defaultValue: 'CH!@#!@', description: 'give number')
        choice(choices: 'Regular\nHofix', description: 'What release is this', name: 'Release')
        password(name: 'my_pass', defaultValue: '', description: 'enter passwd: ')
        credentials(name: 'mycreds', description: 'myDockercreds', required: true)
        
    }
    stage ('prod') {
                steps {
                    echo "*** this is prod stage ***"
                    echo "the ticket is ${params.Release}"
                    echo "creds are ${mycreds}"
                }
    }
}        
