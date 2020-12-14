
node{
  stage('SCM Checkout')
  {
    git 'https://github.com/Bharatsgit/my-app.git'
    
  }
  stage('Compile-Package')
  {
    def mvnHome = tool name: 'maven-3', type: 'maven'
    sh "${mvnHome}/bin/mvn package"
  }
  stage('Mail Notifications')
  {
    
    mail bcc: '', body: 'Jenkins - 12/14/2020 - Bharat Singh', cc: '', from: '', replyTo: '', subject: 'Jenkins - 12/14/2020', to: 'bbspython@gmail.com'
    
  }
}
    
    
