node {
    stage('SCM Checkout') { 
        // Get some code from a GitHub repository
        git 'https://github.com/khaledlim/jenkins-Git-Maven_Devops.git'
    }
    stage('compile-package') {
       // Get the Maven tool.
        mvnHome = tool name: 'maven-3', type: 'maven'
        bat "${mvnHome}/bin/mvn package"   // OS.Windows
        // sh "${mvnHome}/bin/mvn package"   // OS.Linux
    }
    stage('Email Notification') {
        mail bcc: '', body: '''Welcome to "DevOps with Jenkins Pipeline, Ansible, Kubernetes & Docker"
        Thanks''', cc: '', from: '', replyTo: '', subject: '$JOB_NAME -BUILD # $BUILD_NUMBER !', to: 'khaledlimem7@gmail.com'
  
    }
}
