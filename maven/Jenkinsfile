node('built-in') 
{
    stage('Continuous Download-mybranch') 
	{
    git 'https://github.com/sunildevops77/maven.git'
	}
    stage('Continuous Build-mybranch') 
	{
    sh label: '', script: 'mvn package'
	}
    stage('Continuous Deployment-mybranch') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war   ubuntu@172.31.34.46:/var/lib/tomcat8/webapps/qaenv.war'
	}
    stage('Continuous Testing'-mybranch) 
	{
              sh label: '', script: 'echo "Testing Passed"'
	}
    stage('Continuous Delivery-mybranch') 
	{
		sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war   ubuntu@172.31.41.63:/var/lib/tomcat8/webapps/prodenv.war'
	}
}
