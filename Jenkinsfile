node {
    stage('SCM Checkout') { 
        // Get some code from a GitHub repository
        git 'https://github.com/khaledlim/jenkins-Git-Maven_Devops.git'
    }
    stage('compile-package') {
       // Get the Maven tool.
        mvnHome = tool name: 'maven-3', type: 'maven'
        sh "${mvnHome}/bin/mvn package"

    }
}