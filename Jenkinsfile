pipeline
{
    agent any
    
    stages{
        stage('Continous download')
        {
            steps
            {
                git 'https://github.com/gopireddy0194/test.git'
            }
        }
	stage('Validate-again')
	{
		steps
		{
		   sh label: '', script: 'mvn validate'
		}
	}
        stage('compile-again')
        {
            steps
            {
              sh label: '', script: 'mvn compile'  
            }
            
        }
        stage('test')
        {
            steps
            {
                sh label: '', script: 'mvn test'
            }
        }
        stage('final')
        {
            steps
            {
                echo " compiled and tested successfully"
            }
        }
    }
} 
