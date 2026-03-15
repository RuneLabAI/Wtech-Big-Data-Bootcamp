# Oturum 4: Git, Linux, Docker ve Bitirme Projesi Tanıtımı

**Tarih:** 12 Mart 2025 | **Hafta 2** | **Eğitmen:** [Enes Fehmi Manan](https://www.linkedin.com/in/enesfehmimanan/)

---

## Konular

- Git ve versiyon kontrolü: commit, branch, merge, GitHub remote işlemleri
- Linux temel komutları: navigasyon, dosya işlemleri, pipe, redirect, grep
- Docker mimarisi: image, container, Dockerfile yazımı, Docker Compose
- Bitirme projesi tanıtımı, veri seti dağıtımı ve beklentiler

---

## Temel Git Komutları

| Komut | Açıklama |
|-------|----------|
| `git clone <url>` | Repo'yu yerel ortama kopyalar |
| `git status` | Değişikliklerin durumunu gösterir |
| `git add <dosya>` / `git add .` | Değişiklikleri staging'e ekler |
| `git commit -m "mesaj"` | Staging'deki değişiklikleri commit eder |
| `git push` | Commit'leri remote'a gönderir |
| `git pull` | Remote'tan güncellemeleri çeker |
| `git branch` | Mevcut branch'leri listeler |
| `git checkout -b <branch>` | Yeni branch oluşturur ve geçer |
| `git merge <branch>` | Belirtilen branch'i mevcut branch'e birleştirir |

---

## Temel Linux Komutları

| Komut | Açıklama |
|-------|----------|
| `ls` | Dizin içeriğini listeler |
| `cd <dizin>` | Dizin değiştirir |
| `pwd` | Bulunulan dizini gösterir |
| `mkdir <isim>` | Yeni dizin oluşturur |
| `rm <dosya>` | Dosya siler |
| `rm -r <dizin>` | Dizin ve içeriğini siler |
| `cp <kaynak> <hedef>` | Dosya/dizin kopyalar |
| `mv <kaynak> <hedef>` | Taşır veya yeniden adlandırır |
| `cat <dosya>` | Dosya içeriğini gösterir |
| `grep <pattern> <dosya>` | Dosyada arama yapar |
| `chmod +x <dosya>` | Dosyaya çalıştırma izni verir |
| `|` | Bir komutun çıktısını diğerine yönlendirir (pipe) |
| `>` | Çıktıyı dosyaya yazar (redirect) |

---

## Temel Docker Komutları

| Komut | Açıklama |
|-------|----------|
| `docker build -t <isim> .` | Mevcut dizindeki Dockerfile ile image oluşturur |
| `docker run <image>` | Container başlatır |
| `docker run -d <image>` | Container'ı arka planda (detached) çalıştırır |
| `docker run -p 8080:80 <image>` | Port mapping ile çalıştırır |
| `docker ps` | Çalışan container'ları listeler |
| `docker ps -a` | Tüm container'ları listeler |
| `docker stop <container_id>` | Container'ı durdurur |
| `docker rm <container_id>` | Container'ı siler |
| `docker images` | Yerel image'ları listeler |
| `docker rmi <image>` | Image siler |
| `docker-compose up -d` | Compose ile tanımlı servisleri başlatır |
| `docker-compose down` | Compose servislerini durdurur ve kaldırır |

---

## Kaynaklar

- [Git Resmi Dokümantasyon](https://git-scm.com/doc)
- [Docker Resmi Dokümantasyon](https://docs.docker.com/)
- [Linux Command Line Cheatsheet](https://cheatography.com/davechild/cheat-sheets/linux-command-line/)
- [Conventional Commits](https://www.conventionalcommits.org/)
