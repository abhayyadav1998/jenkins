pipeline{
    agent any
parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
environment{
    ENV_URL= 'env.abhay'
}
triggers{

     //cron('H/2 * * * *')
     //Spread load evenly by using ‘H/2 * * * *’ rather than ‘*/2 * * * *’
      }
    stages{
        stage ('stage one'){
            steps{
                echo "Hello world"
            }
        }
        stage ('stage tewo'){
            environment{
               ENV_URL2= 'env.yadav'
                }
            steps{
                echo "Hello world"
            }
        }
        stage ('stage three'){
            environment{
               ENV_URL= 'env.yadav'
                }
            steps{
                sh '''
                echo "Hello world"
                echo "ENV_URL= $ENV_URL"
                echo "ENV_URL2= $ENV_URL2"

                '''
            }
        }
    }
}