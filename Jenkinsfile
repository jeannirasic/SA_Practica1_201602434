node {
	stage('SCM') {
		git branch: 'master', url: 'https://github.com/jeannirasic/SA_Practica1_201602434.git'
	}

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
