pipeline {
    agent any
    tools {maven "mavenV3"}
    stages{
        stage("checkout"){
            steps{
                git branch: "main", url: "https://github.com/edisonso/SpringPetClinic.git"
            }
        }
        stage("build"){
            steps{
                echo "lalala"
                bat "mvn compile"
            }
        }
        stage("test"){
            steps{
                bat "mvn test"
            }
        }
        stage("package"){
            steps{
                bat "mvn package"
            }
        }
        stage("deploy"){
            steps{
                //bat "java -jar .\target\*.jar"
                //bat "java -h"
                //bat "java -jar .\target\*.jar"
                bat "java -jar .\\target\\spring-petclinic-2.1.0.BUILD-SNAPSHOT.jar"
            }
        }
    }
}
