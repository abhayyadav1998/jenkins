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
                echo "ENV_URL2= $ENV_URL"

                '''
            }
        }
    }
}