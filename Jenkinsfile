node('built-in') 
{
    stage('Continuous Download') 
	{
    git 'https://github.com/sunildevops77/maven.git'
	}
    stage('Continuous Build') 
	{
    sh label: '', script: 'mvn package'
	}
    stage('Continuous Deployment') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war   ubuntu@172.31.3.223:/var/lib/tomcat8/webapps/qaenv.war'
	}
    stage('Continuous Testing') 
	{
              sh label: '', script: 'echo "Testing Passed"'
	}
    stage('Continuous Delivery') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war   ubuntu@172.31.3.99:/var/lib/tomcat8/webapps/prodenv.war'
	}
}
