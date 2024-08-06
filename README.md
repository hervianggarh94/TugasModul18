Pekerjaan rumah 16 modul 18, berikut langkah-langkah membuat tugasnya :

1.  Buat tugas Gradle sederhana untuk menerima parameter CLI dan mencetaknya dengan pesan ucapan
2. Proyek skrip Gradle harus dibuat di repositori yang berbeda dan dorong ke GitHub
Berikut adalah langkah-langkah untuk membuat tugas khusus Gradle dan menambahkan pustaka:

- Buat proyek Gradle baru dengan menjalankan perintah "gradle init --type java-library". Ini akan membuat proyek Gradle baru dengan struktur direktori dan file build.gradle awal.
- Buka file build.gradle di direktori root proyek dan copy kode berikut ke build.gradle :

Task greetingTask() {
    doLast {
        String nama = project.hasProperty('nama') ? project.property('nama') : 'Gradle User'
        println "Hello, $nama! Welcome to Gradle World!"
    }
}

- Jalankan perintah melalui fitur terminal intellej idea, berikut perintahnya : "./gradlew greetingTask -Pname=Angga"
- Fitur manajemen dependensi bawaan Gradle. Untuk melakukannya, tambahkan kode berikut ke file build.gradle Anda:

dependencies {
    testImplementation platform('org.junit:junit-bom:5.9.1')
    testImplementation 'org.junit.jupiter:junit-jupiter'
}

- Lakukan push ke GitHub dengan membuat repositori baru dan menjalankan perintah berikut:

- git init
- git add .
- git commit -m "Initial commit"
- git remote add origin https://github.com/hervianggarh94/TugasModul18.git
- git push -u origin master
