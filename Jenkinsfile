pipeline{
    agent any
    environment{
        PATH = "/C:/apache-maven-3.8.6-bin/apache-maven-3.8.6/bin:$PATH"
    }
    stages{
        stage('checkout'){
            steps{
//                 git credentialsId: 'git_credentials', url: 'https://github.com/Aniruddha124/java-hello-world-with-maven.git'
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github access', url: 'https://github.com/Aniruddha124/java-hello-world-with-maven.git']]])
            }
        }
        stage('build'){
            environment{
                PATH = "/C:/Program Files/Git/bin:$PATH"
            }
            steps{
               echo 'building the code....'
               sh 'mvn package'
            }
        }
//         stage('compile'){
//             steps{
//                 bat 'mvn compile'
//             }
//         }
    }
}
