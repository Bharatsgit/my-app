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
	
}
