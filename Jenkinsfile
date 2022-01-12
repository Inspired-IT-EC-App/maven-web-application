node
{
  def mavenHome = tool name: "maven-3.8.4"
  // get the code from github
  stage('CheckoutCode')
  {
  git branch: 'development', credentialsId: '6ce9b417-ae68-4892-9058-ef0666b9897a', url: 'https://github.com/Inspired-IT-EC-App/maven-web-application.git'
  }
  
  // Build the Source code
  
   stage('Build')
   {
     sh "${mavenHome}/bin/mvn clean package"
   }
   
   // Execute SonarQube Report
   
/*
    stage('ExecuteSonarQubeReport')
    {
	  sh "${mavenHome}/bin/mvn clean sonar:sonar" 
	  }
  	
	// Upload Artifact Into the Nexus
	
	stage('UploadArtifactIntoNexus')
	{
	  sh "${mavenHome}/bin/mvn clean deploy" 
	}
   
    // deploy Application To Tomcat Server

    stage('DeployAppToTomcat')
    {
	  sshagent(['01bb01a1-9228-420b-8d4e-302ce1aae877']){
	  sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@3.144.201.197:/opt/apache-tomcat-9.0.56/webapps/"
	  } 
    }
   stage('SendEmailNotification')
  {
   mail bcc: 'thakur5735@gmail.com', body: '''Build Over..

   Regards,
   Mandeep Singh,
   82970''', cc: 'thakur5735@gmail.com', from: '', replyTo: '', subject: 'Build Over..', to: 'thakur5735@gmail.com'
  }
*/
}

