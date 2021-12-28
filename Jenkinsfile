node('master') 
	{
    stage('Continuous download') 
	   {
			git 'https://github.com/rameshn1990/-spring-boot-dockerize.git'
       }
	stage('Continuous build') 
		{
			sh 'mvn clean package'
		}
   
    stage('Build Docker Image')
		{
			
			sh 'docker build -t springbootapp .' 
		}
	
	stage('Run Docker Image')	
    	{
			sh '''docker run --name springboot -p 7070:8080 -d springbootapp'''
		}
	}
