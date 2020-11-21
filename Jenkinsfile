node
{
	stage('SCM Checkout')
	{
	  git 'https://github.com/Bharatsgit/my-app'
	}
	stage('Compile-Package')
	{
	 mvnHome = tool name: 'mvn-33', type: 'maven'
		sh "${mvnHome}/bin/mvn package"
		
	}
	stage('Email Notification')
	{
		mail bcc: '', body: '''Hi,
			This is jenkins from 11-22-2020

		Thanks,
	Bharat Singh''', cc: '', from: '', replyTo: '', subject: 'bharat python 11-22-2020', to: 'bbspython@gmail.com'
	}
	stage('Slack Notifications')
	{
		slackSend channel: '#jenkins-pipeline-11-21-2020', color: 'good', message: 'TestTestTestTestTest - Bharat', tokenCredentialId: 'slack_demo_11_21', username: 'bharatuser'
	}
	
}
