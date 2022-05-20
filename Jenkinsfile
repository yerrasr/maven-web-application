pipeline{

agent any


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
  
}
}	
