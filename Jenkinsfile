node {
	stage('SCM') {
		git branch: 'test', url: 'https://github.com/jeannirasic/SA_Practica1_201602434.git'
	}

	stage('Install') {
		sh "npm install"
	}
	
	
		
	stage('Test') {
		sh "npm run test --watch=false"
	}
		
	stage('Build') {
		sh "npm run build --prod"
	}
		
	stage('Deploy') {
		sh "npm start"
	}
}
