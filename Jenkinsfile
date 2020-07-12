node{
  stage('SCM Checkout'){
    git 'https://github.com/inamdarsaifu/New_Repos'
  }
  stage('Compile-Package'){
    sh 'mvn clean package'
    sh 'mv target/*.jar target/New_Repos.jar'
  }

  stage('Deploy-Dev'){
      sshagent (['aws-user']) {
    	sh 'scp -p StrictHostKeyChecking=no target/*.jar ec2-user@172.31.45.211:/home/ec2-user/Dojo/Deploy_files/'
      }
  }

}
