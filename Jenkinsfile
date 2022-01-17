properties([parameters([string(description: 'enter your name here', name: 'Name'), string(description: 'enter your age here', name: 'Age'), choice(choices: ['Male', 'Female', 'Transgender'], description: 'Choose your gender here', name: 'Gender')])])

pipeline{

agent any

tools{
maven 'Maven 3.8.4'

}

stages{

  stage('CheckOutCode'){
    steps{
    git branch: 'development', credentialsId: '957b543e-6f77-4cef-9aec-82e9b0230975', url: 'https://github.com/devopstrainingblr/maven-web-application-1.git'
	    echo"Your name is ${Name}"
	
	}
  }
  
  stage('Build'){
  steps{
  sh  "mvn clean package"
  }
  }
}

}//Pipeline closing
