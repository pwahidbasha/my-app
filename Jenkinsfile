node{
   stage('SCM Checkout'){
     git 'https://github.com/javahometech/my-app'
   }
   stage('Compile-Package'){
      // Get maven home path
      def mvnHome =  tool name: 'maven', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   }
   stage('Email Notification'){
      mail bcc: '', body: '''Hi Welcome to jenkins email alerts
      Thanks
      Wahid''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'wahidbasha47@gmail.com'
   }
  // stage('Slack Notification'){
    //   slackSend baseUrl: 'https://hooks.slack.com/services/',
     //  channel: '#jenkins-pipeline-demo',
     //  color: 'good', 
      // message: 'Welcome to Jenkins, Slack!', 
      // teamDomain: 'javahomecloud',
      // tokenCredentialId: 'slack-demo'
  // }
}
