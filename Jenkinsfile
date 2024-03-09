pipeline{
    agent any
environment{
    ENV_URL= 'env.abhay'
}
    stages{
        stage ('stage one'){
            steps{
                echo "Hello world"
            }
        }
        stage ('stage tewo'){
            steps{
                echo "Hello world"
                environment{
               ENV_URL2= 'env.rakesh'
                }
            }
        }
        stage ('stage three'){
            steps{
                sh '''
             environment{
               ENV_URL= 'env.yadav'
                }
                echo "Hello world"
                echo "ENV_URL= $ENV_URL"
                echo "ENV_URL2= $ENV_URL"

                '''
            }
        }
    }
}