node
{
	stage('SCM Checkout')
	{
	  git 'tool name: 'mvn-33', type: 'maven'
	}
	stage('Compile-Package')
	{
	 mvnHome = tool name: 'mvn-33', type: 'maven'
		sh "${mvnHome}/bin/mvn package"
		
	}
	
}
