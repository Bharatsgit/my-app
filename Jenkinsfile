node{
stage('SCM Checkout')
	{
		git 'https://github.com/Bharatsgit/my-app.git'
	}
	stage('Compile-Package')
	  {
	  	def mvnHome = tool name: 'mvn2', type: 'maven'
		  sh "${mvnHome}/bin/mvn package"
	  }	
	stage('Email Notifications')
	{
		mail bcc: '', body: '''Hi ,
This is email alerts.

Thanks,
Bharat''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'bbspython@gmail.com'
	}
	stage('Slack Notifications')
	{
		slackSend baseUrl: 'https://hooks.slack.com/services/', 
			channel: '#jenkins-pipeline-demo', color: 'good', 
			message: 'Welcome to Jenkins . Slack !', 
			username: 'bharatjenkins'	
	}
	
    }

	
