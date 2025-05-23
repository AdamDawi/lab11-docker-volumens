## Utworzenie sieci Docker 
```bash
docker network create --driver bridge --subnet 10.0.0.0/24 --gateway 10.0.0.1 lab11net
```
**Działanie polecenia**

![Image](https://github.com/user-attachments/assets/f72ae059-daa4-4a4d-925e-4d4058d790e2)

**Potwierdzenia utworzenia sieci**

![Image](https://github.com/user-attachments/assets/07463733-0db6-4dd1-ab74-1b89e77591cc)

## Uruchamianie kontenerów
### Web1
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

### Web2
```bash
docker run -d --name web2 `
  --network lab11net `
  --ip 10.0.0.11 `
  -p 8082:80 `
  -v "C:\Users\adamd\OneDrive\Pulpit\lab11\web2\html:/usr/share/nginx/html:ro" `
  -v "C:\Users\adamd\OneDrive\Pulpit\lab11\web2\logs:/var/log/nginx" `
  nginx:latest
```

**Działanie polecenia**

![Image](https://github.com/user-attachments/assets/3836323d-81b9-4815-9435-820187c5960d)

**Potwierdzenia działania strony**

![Image](https://github.com/user-attachments/assets/5bdf8b5c-2b0c-4d25-99c9-907f391c8ac3)

### Web3
```bash
docker run -d --name web3 `
  --network lab11net `
  --ip 10.0.0.12 `
  -p 8083:80 `
  -v "C:\Users\adamd\OneDrive\Pulpit\lab11\web3\html:/usr/share/nginx/html:ro" `
  -v "C:\Users\adamd\OneDrive\Pulpit\lab11\web3\logs:/var/log/nginx" `
  nginx:latest
```

**Działanie polecenia**

![Image](https://github.com/user-attachments/assets/db8014ee-ca3d-410e-a3de-06ad7ae220eb)

**Potwierdzenia działania strony**

![Image](https://github.com/user-attachments/assets/90b91b39-e6e4-4e24-90e3-000c601bd06d)