pipeline {
    agent any
    parameters{
        string(name: 'change Ticket', defaultValue: 'CH!@#!@', description: 'give number')
        choice(choice: 'Regular\nHofix', description: 'What release is this', name: 'Release')
        password(name: 'my_pass', defaultValue: '', description: 'enter passwd: ')
    }
    stage ('prod') {
                steps {
                    echo "*** this is prod stage ***"
                }
    }
}        
