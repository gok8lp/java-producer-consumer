# Java Producer–Consumer Exercise

Java'da `Thread`, `Runnable` ve `synchronized` kullanmayı öğrenmek için yazılmış üretici/tüketici denemesi.
A beginner Java concurrency exercise with shared data and synchronized blocks.

## Derleme ve çalıştırma

JDK kurulmuş olmalıdır. Güncel kaynak kökteki `Main.java` dosyasıdır.

```bash
mkdir -p build
javac -d build Main.java
java -cp build Main
```

Program paylaşılan bir sayıyı üretici ve tüketici iş parçacıklarında değiştirir;
çıktı sırası iş parçacığı zamanlamasına bağlıdır.

## Kodda neler var?

- `Main`: paylaşılan nesneyi ve iki iş parçacığını başlatır.
- `producer extends Thread`: ortak sayıyı artırır.
- `consumer implements Runnable`: ortak sayıyı azaltır.
- `synchronized (d)`: aynı nesnenin eşzamanlı erişimini sınırlar.

Bu örnek kuyruk, `wait/notify` veya tamamlanmış bir üretici/tüketici protokolü içermez.
`bayrak` alanı değişmediği için gerçek bir sıra devretme mekanizması değildir.
`untitled/` eski IDE proje kopyasını ve derleme çıktılarını içerir; yukarıdaki komutlar bunları kullanmaz.
