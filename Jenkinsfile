pipeline{

agent any

tools{
maven 'maven3.8.5'

}
	
triggers{
pollSCM('* * * * *')
}

options{
timestamps()
buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5'))
}

stages{

  stage('CheckOutCode'){
    steps{
    git branch: 'master', credentialsId: 'GIT', url: 'https://github.com/yerrasr/maven-web-application.git'
	
	}
  }
 stage('Build'){
  steps{
  sh  "mvn clean package"
   }
  }
  
}
}	
