node('master') 
{
   
   stage('continousdownload') 
   {
       git 'https://github.com/selenium-saikrishna/maven.git'
    }
    
    stage('continousbuild') 
   {
       sh label: '', script: 'mvn package'
    }
    
  stage('continousdeploy') 
   {
       //copying .war file to tomcat server
      sh label: '', script: 'scp /home/new_home/workspace/ScriptedPipeline/webapp/target/webapp.war ubuntu@172.31.20.10:/opt/apache-tomcat-8.5.54/webapps/testevn10.war'
    }
   
   
}
