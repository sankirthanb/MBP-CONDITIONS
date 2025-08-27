pipeline {
    agent any
    parameters{
        string(name: 'change Ticket', defaultValue: 'CH!@#!@', description: 'give number')
        choice(choice: 'Regular\nHofix', description: 'What release is this', name: 'Release')
        password(names: 'my_pass', defaultValue: '', description: 'enter passwd: ')
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
