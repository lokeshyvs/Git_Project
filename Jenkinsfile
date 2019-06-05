node {
    
    
    stage('git project') {
        git credentialsId: 'githubUID', url: 'https://github.com/lokeshyvs/Git_Project.git'
    }
    stage('Email notification') {
        mail bcc: '', body: 'Hi welcome to email alerts in jenkins build', cc: '', from: '', replyTo: '', subject: 'Build Status', to: 'lokeshyvs@gmail.com'
    }
}
def notify(status){
    emailext (
      to: "kumar28bb@gmail.com",
      subject: "${status}: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'",
      body: """<p>${status}: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]':</p>
        <p>Check console output at <a href='${env.BUILD_URL}'>${env.JOB_NAME} [${env.BUILD_NUMBER}]</a></p>""",
    )
 }
