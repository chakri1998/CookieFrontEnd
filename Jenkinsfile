node {
        stage('Checkout SCM'){
                git branch: 'master', url: 'https://github.com/chakri1998/CookieFrontEnd.git'
        }
    
        stage('Install node modules'){
                sh "npm install"
        }
def project_path="Cookie-Project-Angular/e2e/"
        dir(project_path) {
        stage('Build'){
                sh "npm run build"
        }
        stage('Deploy'){
                sh "pm2 restart all"
        }
        }
}
