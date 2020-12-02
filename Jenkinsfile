node{
	stage('SCM CHECKOUT')
	{
		git 'https://github.com/Bharatsgit/my-app.git'
	}
	stage('Compile-Package')
	{
	def mvnHome = tool name: 'maven_12-2', type: 'maven'
		sh "${mvnHome}/bin/mvn package"
	}
	stage('Email Notifications')
	{
		mail bcc: '', body: 'this is year 2020 from Jenkins pipeline 12.2.2020', 
			cc: '', from: '', replyTo: '', 
			subject: 'FROM JENKINS on 12_2_2020', 
			to: 'bbspython@gmail.com'
	}
}
