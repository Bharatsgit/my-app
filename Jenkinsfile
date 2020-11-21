node{
	stage('SCM Checkout')
	{
		git 'https://github.com/Bharatsgit/my-app'
	}
	stage('compile-package')
	      {
		 def mvnHome = tool name: 'mvn3', type: 'maven'
		      sh '${mvnHome}/bin/mvn package'
	      }
	      
}
