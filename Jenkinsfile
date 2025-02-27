pipeline{
    agent any
        stages{
            stage("step") {
                steps{
                    echo " this pipeling script have parameters and Environment variable"
                }

           }
           environment{
            name = "This is parameterized script"
           }
           stage("Deployment"){
                when {
                    "$(params.action)" == 'apply'
                steps{
                    echo " terrafrom init"
                }
            }
           }
            }     
       parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'action', choices: ['apply', 'destroy'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }  
    }
