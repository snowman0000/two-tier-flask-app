pipeline{
    agent any
    stages{
        stage("build"){
            steps{
                git url: 'https://github.com/snowman0000/two-tier-flask-app.git', branch: 'master'
            }
            
        }
          stage("test"){
            steps{
                sh "docker build -t flaskapp ."
            }
    }
        stage("deploy"){
            steps{
                sh "docker compose up -d --build"
            }
        }
    }
  
}
