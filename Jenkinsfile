//SCRIPTED

//DECLARATIVE AGENT
// agent is similar to node but it gives a lot of flaxability 

// node {
// 	echo "Byild"
// 	echo "Test"
// 	echo "Inregration Test"

// }
pipeline{
agent any
stages{
	stage('Build'){
		steps{
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