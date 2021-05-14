pipeline
{
    agent any
    
    stages{
        stage('Continous download1')
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
        stage('compile-1')
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
		sh label: '', script: 'mvn package'
                echo " compiled and tested and packaged successfully using webhook6"
            }
        }
    }
} 
