pipeline{
    agent any
    tools {
  maven 'maven'
}

    parameters {
  string defaultValue: 'main', description: 'branch to build', name: 'BRANCH'
}
    stages{
       
        stage('build application'){
            steps{
                
                withCredentials([string(credentialsId: 'DB_PASSWORD', variable: 'DB_PASSWORD')]) {
    sh "mvn clean package"
    
}
                
            }
        }
    }
}
