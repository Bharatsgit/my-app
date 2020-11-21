node{
	stage('SCM Checkout')
	{
		git 'https://github.com/Bharatsgit/my-app'
	}
	stage('compile-package')
	      {
		 def mvnHome = tool name: 'mvn3', type: 'maven'
		 sh "${mvnHome}/bin/mvn package"
	      }
	stage('Email Notifications')
	{
	mail bcc: '', body: '''Hi from Jenkins Alerts. 11-21
	Thanks
	Bharat''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job Completion', to: 'bbspython@gmail.com'
	}
}
