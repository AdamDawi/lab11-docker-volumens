## Utworzenie sieci Docker 
```bash
docker network create --driver bridge --subnet 10.0.0.0/24 --gateway 10.0.0.1 lab11net
```
**Działanie polecenia**
![Image](https://github.com/user-attachments/assets/f72ae059-daa4-4a4d-925e-4d4058d790e2)

**Potwierdzenia utworzenia sieci**
![Image](https://github.com/user-attachments/assets/07463733-0db6-4dd1-ab74-1b89e77591cc)

## Uruchamianie kontenerów
**Web1**
```bash
docker run -d --name web1 `
  --network lab11net `
  --ip 10.0.0.10 `
  -p 8081:80 `
  -v "C:\Users\adamd\OneDrive\Pulpit\lab11\web1\html:/usr/share/nginx/html:ro" `
  -v "C:\Users\adamd\OneDrive\Pulpit\lab11\web1\logs:/var/log/nginx" `
  nginx:latest
```

**Działanie polecenia**
![Image](https://github.com/user-attachments/assets/3f052be4-e487-42f8-9a78-9bf603382e5f)

**Potwierdzenia działania strony**
![Image](https://github.com/user-attachments/assets/d3118b28-15b8-4f4e-b5c1-131d7cfffeb4)