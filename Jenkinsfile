node {
    
   
    stage('git project') {
        git credentialsId: 'githubUID', url: 'https://github.com/lokeshyvs/Git_Project.git'
    }
    stage('Email notification') {
        notify('Status')
    }
}
def notify(status){
    emailext (
      to: 'lokeshyvs@gmail.com',
      subject:"Job '${JOB_NAME}' (${BUILD_NUMBER}) is waiting for input",
      body: "<p>${status}: Job "
    )
 }
