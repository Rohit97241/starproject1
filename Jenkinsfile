pipeline {
    agent any
    stages{
        stage('build project'){
            steps{
                git url:'https://github.com/Rohit97241/starproject1/', branch: "master"
                sh 'mvn clean package'
              
            }
        }
        stage('Build docker image'){
            steps{
                script{
                    sh 'docker build -t Rohit97241/staragileprojectfinance:v1 .'
                    sh 'docker images'
                }
            }
        }
         
        
     stage('Deploy') {
            steps {
                sh 'sudo docker run -itd --name My-first-containe21211 -p 8083:8081 Rohit97241/staragileprojectfinance:v1'
                  
                }
            }
        
    }
}
