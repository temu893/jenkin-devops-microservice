//SCRIPTED

//DECLARATIVE AGENT
// agent is similar to node but it gives a lot of flaxability 

// node {
// 	echo "Byild"
// 	echo "Test"
// 	echo "Inregration Test"

// }
pipeline{
//for any ahent 
agent any

//for node docker image
//agent{ docker { image 'maven:3.6.3'}}
//
enviroment{
	dockerHome = tool 'myDocker'
	mavenHome = tool 'myMaven'
	PATH = '$dockerHome/bin:$mavenHome/bin:$PATH'
}
stages{
	stage('Build'){
		steps{
		
			sh 'mvn --version'
			sh 'docker version'
			echo "Build"
			echo "PATH - $PATH"
			echo "BUILD_NUMBER - $env.BUILD_NUMBER"
			echo "BUILD_ID - $env.BUILD_ID"
			echo "JOB_NAME - $env.JOB_NAME"
			echo "BUILD_TAG - $env.BUILD_TAG"
			echo "BUILD_URL - $env.BUILD_UEL"


		}
	}
		stage('Test'){
		steps{
			echo "Test"
		}
	}
		stage('Integration Test'){
		steps{
			echo "Integration Test"
		}
	}
}
post{
	always{
		echo 'Im awesone. I run always'
	}
	success{
		echo 'I run when you are successful'
	}
	failure{
		echo 'I run when you fail'
	}
}
}