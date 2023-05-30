pipeline {
 agent any
 stages {
 stage('Checkout') {
 steps {
 // Clonar el repositorio
 git 'https://github.com/tu-usuario/tu-repositorio.git'
 }
 }stage('Install Dependencies') {
 steps {
 // Crear un entorno virtual
 sh 'python -m venv venv'

 // Activar el entorno virtual
 sh 'source venv/bin/activate'

 // Instalar dependencias con pip
 sh 'pip install -r requirements.txt'
 
 }
 }

 stage('Run Tests') {
 steps {
 // Ejecutar pruebas con pytest 
 sh 'pytest'
 }
 }

 stage('Build') {
 steps {
 // Realizar cualquier operación de construcción adicional
 // Por ejemplo, generar archivos o ejecutar tareas de compilación
 // sh 'python build.py'
 }
 }

 stage('Deploy') {
 steps {
 // Realizar el despliegue de la aplicación
 // Puedes personalizar este paso según tus necesidades
 // Por ejemplo, copiar archivos a un servidor de producción
 // sh 'scp -r dist user@servidor:/ruta/destino'
 }
 }
 }
}