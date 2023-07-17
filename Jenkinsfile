pipeline {
    agent {
    label 'windows'
    }

    stages {
        stage('Checkout') {
            steps {
                // Étape de récupération du code source depuis un référentiel Git
                git 'https://github.com/mamadoucire/angular.git'
            }
        }

     /*   stage('Install Dependencies') {
            steps {
                // Étape d'installation de Composer
                bat 'php --version'
                bat 'php -r "copy(\'https://getcomposer.org/installer\', \'composer-setup.php\');"'
                bat 'php composer-setup.php'
                bat 'php -r "unlink(\'composer-setup.php\');"'
                bat 'php composer.phar clear-cache'
                bat 'php composer.phar self-update'
                // Étape d'installation des dépendances via Composer
                bat 'php composer.phar install'
            }
        }*/

      /*  stage('Installation de angular cli et node js'){
            steps{
                // Installation de Node.js v16.20.0
                bat 'curl -sL https://nodejs.org/dist/v16.20.0/node-v16.20.0-x64.msi -o nodejs.msi'
                bat 'msiexec /i nodejs.msi /quiet'
        
               // Installation d'Angular CLI 15.2.4
               bat 'npm install -g @angular/cli@15.2.4'
               
               // Lien symbolique pour Angular CLI
               bat 'npm link @angular/cli'
               // Vérification des versions installées
               bat 'node -v'
               bat 'setx PATH "%PATH%;%APPDATA%\\npm"'
               bat 'ng --version'
            }
        }*/
      /*  stage('Test') {
            steps {
                sh './vendor/bin/phpunit'
            }
        }*/

      stage('Build') {
            steps {
                // Étape de construction de votre projet PHP (par exemple, exécution de tests, génération de fichiers, etc.)
                bat 'ng build --configuration'
                bat 'npm install -g @angular/cli'
                bat 'ng new test'
                bat 'cd test'
                bat 'ng serve'
                 // bat 'php build.php'
            }
        }

      /*  stage('Deploy') {
            steps {
                // Étape de déploiement de votre projet PHP (par exemple, copie des fichiers sur un serveur distant)
                bat 'xcopy /E /I /Y src\ dist\'
                // ou utilisez d'autres commandes spécifiques à votre processus de déploiement
            }
        }*/
    }
}
