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
            }
        }
        stage ('stage three'){
            steps{
                sh '''
                echo "Hello world"
                echo "ENV_URL= $ENV_URL"

                '''
            }
        }
    }
}