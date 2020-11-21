node{
	stage('SCM Checkout')
	{
		git 'https://github.com/javahometech/my-app.git'
	}
	stage('compile-package')
	      {
		 def mvnHome = tool name: 'mvn3', type: 'maven'
		      sh '${mvnHome}/bin/mvn package'
	      }
	      
}
