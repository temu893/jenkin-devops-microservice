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
//**agent any

//for node docker image
agent{ docker { image 'node:18.8'}}

stages{
	stage('Build'){
		steps{
			//sh 'node --version'
			sh 'node --version'
			echo "Build"
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