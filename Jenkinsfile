pipeline{
    agent any
    parameters{
        choice(name: 'ENV', choices: ['Dev', 'Prod'], description: 'chose the environment')
        string(name: 'COMPONENT', defaultvalue: 'mongodb', description: 'Enter the name of the component')
    }
    environment{
        SSH_CRED = credentials ('SSH-Centos7')  
    }
    stages{
        stage('Lint checks'){
            when {branch pattern: 'feature-.*', comparator: "REGEXP"}
            steps{
                sh "env"
                sh "echo Style checks"
                sh "echo running is feature branch"  
            
             }
        }
        stage('Do a dry-run'){  //this will only execute only when you raise the PR
            steps{
                sh "env"  // just to see the envirment variables to see the envirnoment variable as a part of the pipeline
                sh "ansible-playbook robot-dryrun.yml ansible_usr=${SSH_CRED_USR} ansible_password=${SSH_CRED_PSW} -e COMPONENT=${params.COMPONENT} -e ENV=${params.ENV}"

            }
        }
        stage('Promote to Prod')
        when { branch 'main'}
        steps{
            sh "echo runs only when you pushed the git tag"
        }
    }
    
}