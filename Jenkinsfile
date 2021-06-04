pipeline {
    agent any

    stages {
        stage('Install') {
		sh 'npm i'
	}
		
	stage('Test') {
		sh 'npm run test-headless'
	}
		
	stage('Build') {
		sh 'npm run build --prod'
	}
		
	stage('Deploy') {
		sh 'npm start'
	}
    }
}
