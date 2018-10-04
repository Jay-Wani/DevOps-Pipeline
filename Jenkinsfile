pipeline {
    agent any
    stages{
        stage('Init'){
            steps {
                echo "testing the package..."
            }
        }

        stage('Build'){
            steps {
                echo "building the package....."
            }    
        }
               
        
        stage('Deploy to Staging'){
            steps {
                echo "deploying the package to staging ..."
            }
        }


        stage('Deploy to Prod'){
              steps{
                timeout(time:5, unit:'DAYS'){
                    input message:'Approve PRODUCTION Deployment ....?'
                }

                echo "Deploying to Prod post approval from management......"
              }
        }
    }
}