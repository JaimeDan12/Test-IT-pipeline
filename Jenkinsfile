pipeline {
	agent  any
	// agent { docker { image 'maven:3.6.3'} }

	stages{
		stage('Build'){
			steps{
				echo 'Build'
			}
		}
		stage('Test'){
			steps{
				echo 'Test'
			}
		}
		stage("Test intégration"){
			steps{
				echo "Test integration"
			}
		}
		// stage('Build Docker Image'){
		// 	steps{
		// 		script{
		// 			dockerImage = docker.build("danjaime/currency-exchange-devops/general:${env.BUILD_TAG}")
		// 		}
		// 	}
		// }
		// stage('Push Docker Image'){
		// 	steps{
		// 		script{
		// 			docker.withRegistry('','dockerhub'){
		// 				dockerImage.push()
		// 				dockerImage.push('latest')
		// 			}
		// 		}
		// 	}
		// }
	}
	post{
		always{
			echo "Je suis genial. Je fonctionne toujours!"
		}
		success{
			echo "Je fonctionne quant tu reussi!"
		}
		failure {
			echo "Je suis ici quand tu echoue!"
		}
	}
}

// pipeline {
//     agent any
//     stages {
//         stage('Build') {
//             agent {
//                 docker {
//                     image 'gradle:6.7-jdk11'
//                     // Run the container on the node specified at the
//                     // top-level of the Pipeline, in the same workspace,
//                     // rather than on a new node entirely:
//                     reuseNode true
//                 }
//             }
//             steps {
//                 sh 'gradle --version'
//             }
//         }
 // }

