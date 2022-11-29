pipeline{
    agent any
    environment{
        PATH = "/C:/apache-maven-3.8.6-bin/apache-maven-3.8.6/bin:$PATH"
    }
    stages{
        stage('checkout'){
            steps{
                git credentialsId: 'git_credentials', url: 'https://github.com/Aniruddha124/java-hello-world-with-maven'       
            }
        }
        stage('build'){
            steps{
               echo 'building the code....'
               bat 'mvn clean'
            }
        }
        stage('compile'){
            steps{
                bat 'mvn compile'
            }
        }
    }
}
