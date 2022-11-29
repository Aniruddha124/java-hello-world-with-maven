pipeline{
    agent any

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
