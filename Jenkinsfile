node {
	stage('SCM') {
		git branch: 'test', url: 'https://github.com/jeannirasic/SA_Practica1_201602434.git'
	}

	stage('Install') {
		sh "npm install"
	}
	
	stage('Nvm') {
		sh "curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.0/install.sh | bash"
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
