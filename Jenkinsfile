node{
  stage('SCM Checkout'){
    git 'https://github.com/inamdarsaifu/New_Repos'
  }
  stage('Compile-Package'){
    sh 'mvn clean package'
    sh 'mv target/*.jar target/New_Repos.jar'
  }


}
