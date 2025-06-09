# a428-cicd-labs-jenkins

Proyek ini dibuat sebagai bagian dari pembelajaran Continuous Integration/Continuous Deployment (CI/CD) menggunakan Jenkins. Dalam repositori ini, pipeline Jenkins didefinisikan menggunakan `Jenkinsfile` yang dijalankan otomatis setelah integrasi dengan GitHub berhasil dilakukan.

## Tujuan

- Men-setup Jenkins secara lokal
- Menghubungkan Jenkins ke repository GitHub
- Membuat pipeline otomatis menggunakan Jenkinsfile
- Menjalankan tahapan Build, Test, dan Deploy secara otomatis

## Langkah-langkah

### 1. Clone Repository

Repository hasil fork di-clone ke lokal:

git clone https://github.com/rinogabriel/a428-cicd-labs-jenkins.git


### 2. Setup Jenkins

- Jenkins diinstal secara lokal
- Plugin yang digunakan: Git, Pipeline
- Jenkins dijalankan melalui browser: `http://localhost:8080`

### 3. Integrasi GitHub ke Jenkins

- Membuat Jenkins job bertipe *Pipeline*
- Menentukan Source Code Management → Git
- Mengisi Repository URL:

https://github.com/rinogabriel/a428-cicd-labs-jenkins.git

- Branch: `react-app`

### 4. Menambahkan Jenkinsfile

File `Jenkinsfile` ditambahkan ke root folder dengan isi sebagai berikut:

pipeline {
agent any

stages {
    stage('Build') {
        steps {
            echo 'Building...'
        }
    }
    stage('Test') {
        steps {
            echo 'Testing...'
        }
    }
    stage('Deploy') {
        steps {
            echo 'Deploying...'
        }
    }
}
}

### 5. Menjalankan Pipeline

- Jenkins otomatis mendeteksi `Jenkinsfile` dan menjalankan pipeline
- Tahap Build, Test, dan Deploy berhasil dijalankan di Jenkins console

## Status Proyek

- [x] Repository berhasil terhubung ke Jenkins
- [x] Jenkinsfile berhasil dieksekusi
- [x] Pipeline berjalan dengan tahapan yang sudah didefinisikan

## Struktur Folder

a428-cicd-labs-jenkins/
├── Jenkinsfile
└── README.md

## Author

Rino Gabriel  
Proyek ini dikerjakan sebagai bagian dari tugas/lab CI/CD menggunakan Jenkins.

## Catatan

Untuk mencoba proyek ini:

1. Install Jenkins secara lokal
2. Fork dan clone repository ini
3. Tambahkan Jenkinsfile jika perlu
4. Jalankan build pipeline dari Jenkins dashboard