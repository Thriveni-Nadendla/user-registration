pipeline{
    agent any
    tools {
  maven 'maven'
}

    parameters {
  string defaultValue: 'main', description: 'branch to build', name: 'BRANCH'
}
    stages{
        stage('clone repository'){
            steps{
                git branch: "${params.BRANCH}", credentialsId: 'github-cred', url: 'git@github.com:Thriveni-Nadendla/user-registration.git'
            }
        }
        stage('build application'){
            steps{
                
                withCredentials([string(credentialsId: 'DB_PASSWORD', variable: 'DB_PASSWORD')]) {
    sh "mvn clean package"
    
}
                
            }
        }
    }
}
