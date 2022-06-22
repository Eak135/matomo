pipeline {
  agent any
  stages {
    // Извлекаем проект из Bitbucket 
    stage('Checkout') { }
    // Собираем проект. Получаем на выходе пакетный файл AUDIT_Import_ALL.ispac 
    stage('Build') { }
    // Загружаем архив с проектом на удаленный сервер. Деплоим его на MS SQL Server 
    stage('Deploy') { }
  }
}
