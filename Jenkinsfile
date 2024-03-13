// pipeline{
//     agent any
// parameters {
//         string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

//         text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

//         booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

//         choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

//         password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
//     }
// environment{
//     ENV_URL= 'env.abhay'
// }
// triggers{

//      cron('* * 1 9 *')
//      //Spread load evenly by using ‘H/2 * * * *’ rather than ‘*/2 * * * *’
//       }
// tools {
//         maven 'maven-3.8.5' 
//     }
//     stages{
//         stage ('stage one'){
//             steps{
//                 sh '''
//                 echo "Hello world"
//                 mvn --version
//                 '''
//             }
//         }

   
//         stage('two'){
//             when {environment name: 'CHOICE', value: 'One'}
//             steps{
//                 echo "this massage is from choice ONE"
//             }

//         }
    
//         // stage ('stage two'){
//         //     input {
//         //         message "Are you sure ? you would like to continue if yes did you confirm eith Devops Lead"
//         //         ok "Yes, we should."
//         //         submitter "alice,bob"
//         //         parameters {
//         //             string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
//         //         }
//         //     }?
//         stage ('stage three'){
//             environment{
//                ENV_URL= 'env.yadav'
//                 }
//             steps{
//                 sh '''
//                 echo "Hello world"
//                 echo "ENV_URL= $ENV_URL"
//                 echo "ENV_URL2= $ENV_URL2"

//                 '''
//             }
//         }
//     }
// }

pipeline{
    agent any
    stages{
        stage('parallel stage') {
        parallel {
        stage('one'){
            steps{
                sh '''
                sleep 3
                '''
            }
         }
         stage('two'){
            steps{
                sh '''
                sleep 5
                '''
            }
         }
         stage('three'){
            steps{
                sh '''
                sleep 7
                '''
            }
          }
         }
     }
        stage('four'){
            steps{
                sh '''
                sleep 10
                '''
            }
        }
    }
}