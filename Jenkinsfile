node {
        stage('Checkout SCM'){
                git branch: 'master', url: 'https://github.com/chakri1998/CookieFrontEnd.git'
        }
    def project_path="Cookie-Project-Angular/"
        dir(project_path) {
        stage('Install node modules'){
                sh "npm install"
        }
        stage('Build'){
                sh "npm run build:ssr"
        }
        stage('Deploy'){
                sh "pm2 restart all"
        }
        }
}
