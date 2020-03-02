node {
        stage('Checkout SCM'){
                git branch: 'master', url: 'https://github.com/chakri1998/CookieFrontEnd.git'
        }
    
        stage('Install node modules'){
                sh "npm install"
        }
        stage('Build'){
                sh "cd Cookie-Project-Angular/e2e/"
                sh "npm run build"
        }
        stage('Deploy'){
                sh "pm2 restart all"
        }
        
}
