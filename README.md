# Kafka Exercise 02 – Docker Setup

##  Proje Tanımı
Bu projede Apache Kafka ve Zookeeper'ı Docker ve Docker Compose kullanarak Google Cloud Platform (GCP) üzerinde bir VM instance'ında çalıştırdım. Kafka üzerinde `test-topic` adında bir topic oluşturulmuş ve başarılı bir şekilde listelenmiştir.

---

##  Yapılan Adımlar
1. Google Cloud üzerinde Debian tabanlı bir VM oluşturuldu.
2. Docker ve Docker Compose yüklendi.
3. Kafka ve Zookeeper servisleri için `docker-compose.yml` dosyası yazıldı.
4. Docker container'ları başarıyla ayağa kaldırıldı.
5. Kafka container'ı içerisine girilerek `test-topic` isimli bir topic oluşturuldu ve doğrulandı.
6. GCP üzerinde gerekli VPC Firewall kuralları açıldı (`9092` ve `2181` TCP portları).

---

##  Proje Dosyaları
- `docker-compose.yml` → Kafka ve Zookeeper'ı ayağa kaldıran Docker Compose dosyası.
- `screenshots/` → Terminal çıktıları ve GCP ayarlarına ait ekran görüntüleri.
- `README.md` → Bu doküman.

---

## ⚙ Kurulum ve Kullanım

**Docker Compose ile Kafka ve Zookeeper'ı başlatmak:**

sudo docker-compose up -d

**Çalışan container'ları kontrol etmek:**

sudo docker ps

**Kafka container'ına giriş yapmak:**

sudo docker exec -it kafka bash

**Topic oluşturmak:**

kafka-topics --create --topic test-topic --bootstrap-server kafka:29092 --partitions 1 --replication-factor 1

**Mevcut topic'leri listelemek:**

kafka-topics --list --bootstrap-server kafka:29092

**✔️ Beklenen çıktı:**

test-topic

---

##  Ekran Görüntüleri
- **docker-compose.png** → Docker Compose dosyasının içeriği
- **kafka-ps.png** → Çalışan container'ların listesi
- **kafka-test-topic.png** → Kafka topic oluşturma ve listeleme çıktısı
- **firewall.png** → GCP üzerinde açılan portların firewall kuralı

---

## ✍ Hazırlayan
**İlker Öztürk** — Bahçeşehir Üniversitesi  
GitHub: [https://github.com/ilkeroztr](https://github.com/ilkeroztr)
