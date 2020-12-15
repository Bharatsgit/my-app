
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
  stage('Slack Notifications')
  {
    slackSend baseUrl: 'https://hooks.slack.com/services/', 
      channel: '#jenkins-pipeline_12_14_2020', 
      color: 'good', message: 'welcome to slack 12_14_2020 !', 
      tokenCredentialId: 'slack_demo12_14', 
      username: 'slack_12_14 '
  }
}
    
    
