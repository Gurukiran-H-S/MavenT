pipeline{
	agent any
	tools{
		maven 'Maven'
		jdk 'JDK'
	}
	
	Stages{
		stage('checkout'){
			steps{
			git branch:'main', url: 'https://github.com/Gurukiran-H-S/MavenT.git'
			}
		}
		stage('Build'){
			steps{
			sh 'mvn clean package'
			}
		}
		stage('Test'){
			steps{
			sh 'mvn test'
			}
		}
		stage('Run Application'){
			steps{
			sh 'java -jar target/MavenT-1.0-SNAPSHOT.jar'
		}
	}
	}
	post{
		success{
			echo 'Build sucessfully'
		}
		failure{
			echo 'build failure'
		}
	}
}
