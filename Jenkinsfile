node {
	stage('SCM') {
		git branch: 'test', url: 'https://github.com/jeannirasic/SA_Practica1_201602434.git'
	}

	stage('Install') {
		sh "npm install"
	}
	
	stage('Nvm') {
		sh '''
			curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.0/install.sh | bash
			export NVM_DIR="$HOME/.nvm"
			[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
			[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"
			nvm --version
			nvm install 14.15
			nvm use 14.15
		'''
	}
		
	stage('Test and build') {
		sh '''npm run test --watch=false
		npm run build --prod
		'''
	}
		

	stage('Deploy') {
		sh "npm start"
	}
}
