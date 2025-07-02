# Kafka Exercise 02 – Docker Setup

##  Proje Tanımı
Bu projede Apache Kafka ve Zookeeper'ı Docker kullanarak Google Cloud VM üzerinde çalıştırdım. Kafka üzerinde bir topic oluşturup başarıyla çalıştırdım.

---

##  Yapılan Adımlar

1. Google Cloud üzerinde bir VM oluşturuldu.
2. VM'ye Docker ve Docker Compose kuruldu.
3. Kafka ve Zookeeper için `docker-compose.yml` dosyası oluşturuldu.
4. Docker container'ları başarıyla başlatıldı.
5. Kafka içinde `test-topic` adında bir topic oluşturuldu ve listelendi.
6. GCP üzerinde gerekli VPC firewall kuralları eklendi.

---

## 🗂 Proje Dosyaları

- `docker-compose.yml` → Kafka ve Zookeeper'ı ayağa kaldıran dosya.
- `screenshots/` → Terminal çıktıları ve GCP ayarlarına ait ekran görüntüleri.
- `README.md` → Proje açıklaması.

---

##  Kurulum ve Kullanım

```bash
sudo docker-compose up -d
sudo docker ps
