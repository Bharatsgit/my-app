node{
	stage('SCM CHECKOUT')
	{
		git 'https://github.com/Bharatsgit/my-app.git'
	}
	stage('Compile-Package')
	{
	def mvnHome = tool name: 'maven_12-2', type: 'maven'
		sh "{mvnHome}/bin/mvn package
	}
}
