# Reflection
## What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?
### Jmeter
- Digunakan untuk stress test, load test, dan benchmark dari sebuah API pada website
- Membantu untuk menentukan user load yang berbeda-beda
### Intelij Profiler
- Memberikan detail analisis performance pada kode yang ditulis
- Membantu untuk menganalisis isu pada cpu, memory, dan thread.

## How does the profiling process help you in identifying and understanding the weak points in your application?
- Profiling menganalisis kinerja aplikasi untuk mengidentifikasi penggunaan CPU, memori, dan eksekusi kode yang tidak efisien. Dengan alat seperti IntelliJ Profiler, pengembang dapat menemukan bottleneck, kebocoran memori, dan masalah thread. Selain itu, profiling membantu mengoptimalkan query database dan operasi I/O untuk meningkatkan respons aplikasi. Hasilnya, aplikasi menjadi lebih cepat, stabil, dan efisien.

### Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?
- Ya, IntelliJ Profiler sangat efektif dalam membantu saya mengidentifikasi bottleneck karena profiler ini dapat menemukam metode yang membutuhkan eksekusi paling lama, mendeteksi kebocoran memori, menganalisis performa thread, dan juga mengoptimalkan CPU agar aplikasi berjalan lebih responsif

### What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?
- Karena baru pertama kali melakukan performance testing dan profiling di IntelliJ, saya masih belum terbiasa dengan informasi yang ditampilkan oleh profiler. Beragam data teknis seperti stack trace, alokasi memori, serta grafik CPU dan memori membuat saya kesulitan menentukan bagian mana yang menjadi beban bagi program. Untuk mengatasinya, saya berusaha lebih sering berinteraksi dengan profiler serta memanfaatkan fitur flame graph, yang dirancang agar pengguna lebih mudah mengidentifikasi kelemahan dalam kode.
 
### What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?
- Dengan IntelliJ Profiler, saya dapat dengan cepat menemukan bottleneck dan inefisiensi dalam kode berdasarkan waktu eksekusi metode atau fungsi. Selain itu, saya bisa memantau alokasi memori secara real-time serta aktivitas thread. Profiling di IntelliJ juga intuitif dan mudah digunakan karena terintegrasi langsung dengan IntelliJ IDEA.

### How do you handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?
- Jika menemukan perbedaan hasil, pertama-tama saya akan memastikan bahwa pengujian di IntelliJ Profiler dilakukan dalam kondisi yang sama seperti di JMeter, seperti jumlah thread untuk memastikan beban aplikasi tetap konsisten. Perbedaan jumlah thread atau pengguna pada tiap profiler dapat memengaruhi hasil pengujian. Selain itu, saya juga akan memeriksa kembali rute ke URL localhost di JMeter agar sesuai dan akurat dengan apa yang ingin diuji.

### What strategies do you implement in optimizing application code after analyzing results from performance testing and profiling? How do you ensure the changes you make do not affect the application's functionality?
- Karena metode `getAllStudentsWithCourses()` di StudentService.java merupakan yang paling banyak memakan waktu saat program berjalan, saya mengoptimalkannya dengan mengganti seluruh isi metode dengan return `studentCourseRepository.findAll()`. Perubahan ini menghilangkan loop yang berlebih tanpa mengubah fungsionalitas. Setelah itu, saya menganalisis metode lain yang juga memakan waktu lama, seperti `findStudentWithHighestGpa()` dan `joinStudentNames()`, lalu menerapkan optimasi pada keduanya. Setelah optimasi dilakukan, saya menjalankan kembali profiler dan melihat bahwa waktu eksekusi metode-metode tersebut telah berkurang. Untuk memastikan tidak ada perubahan fungsional, saya menjalankan metode-metode tersebut dan membandingkan hasilnya dengan versi sebelumnya. Namun, best practice yang lebih disarankan adalah melakukan pengujian sebelum dan sesudah optimasi untuk memastikan fungsionalitas tetap sama.

## Jmeter Using CMD
before optimize:
![after_txt](https://github.com/user-attachments/assets/ddbefe48-31a6-404f-bbeb-5d2408286cfe)
after optimize:
![image](https://github.com/user-attachments/assets/b3fc6c42-308f-4b7b-9f91-433b00f850fe)

before optimize:
![Screenshot 2025-03-14 154622](https://github.com/user-attachments/assets/eac81646-98be-49d6-9cb2-92fdb1101dff)

after optimize:
![highest gpa after](https://github.com/user-attachments/assets/8cc88349-a76b-4d55-8e93-077b8dda87b8)

before optimize:

after optimize









