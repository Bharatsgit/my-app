node{
	stages('SCM Checkout')
	{
		git 'https://github.com/javahometech/my-app.git'
	}
	stage('compile-package')
	      {
		 sh 'mvn clean package'
	      }
	      
}
