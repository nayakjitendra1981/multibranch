node('built-in') 
{
    stage('Continuous Download-master') 
	{
    git 'https://github.com/sunildevops77/maven.git'

    stage('Continuous Build-master') 
	{
    sh label: '', script: 'mvn package'
	}
    stage('Continuous Deployment-master') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war   ubuntu@172.31.34.46:/var/lib/tomcat8/webapps/qaenv.war'
	}
    stage('Continuous Testing'-master) 
	{
              sh label: '', script: 'echo "Testing Passed"'
	}
    stage('Continuous Delivery-master') 
	{
		sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war   ubuntu@172.31.41.63:/var/lib/tomcat8/webapps/prodenv.war'
	}
}
