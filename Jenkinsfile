pipeline{
    agent any
     parameters {
         choice(name: 'action', choices: ['apply', 'destroy'], description: 'Pick something')
        }  
    
     environment{
            name = "This is parameterized script"
           }
    stages{
            stage("step") {
                steps{
                    echo " this pipeling script have parameters and Environment variable"
                }

           }
       
           stage("Deployment") {
                when {
                    expression{
                    params.action == 'apply'
                    }
                }
                steps{
                    echo " terrafrom init"
                }
            }
           }
            }     
       
