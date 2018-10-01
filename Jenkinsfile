pipeline {
    agent any
    stages{
        stage('Init'){
            steps {
                echo "testing..."
            }
        }

        stage('Build'){
            def Build = false;
	        try {
		        input message: 'Build?', ok: 'Build'
		        Build = true
		        } catch (err) {
		        Build = false
		        currentBuild.result = 'SUCCESS'
	            }
	
            if (Build){   
	            echo "Building..."
                
                }       
            }	
        
               
        
        stage('Deploy'){
            steps {
                echo "deploying..."
            }
        }

    }
}