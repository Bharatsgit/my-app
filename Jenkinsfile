node{
  stage('SCM Checkout')
  {
    git 'https://github.com/javahometech/my-app.git'
  }
  stage('compile-package')
  {
    def mvnHome = tool name: 'maven-3', type: 'maven'
    sh "${mvnHome}/bin/mvn package"
  }
  stage('Email Notifications')
  {
    emailext body: 'bharat singh - 1/28', subject: 'test email', to: 'bbspython@gmail.com'
  }
}
  
