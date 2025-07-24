<p align="center">
  <img height="100" height="auto" src="https://github.com/freshe4qa/waku/assets/85982863/581b9ed1-ac04-44b4-bfae-017073221624">
</p>

# Waku - Testnet

Official documentation:
>- [Guide](https://docs.waku.org/guides/nwaku/run-node/)

Explorer:
>- [Explorer](-)

### Minimum Hardware Requirements
 - 2x CPUs; the faster clock speed the better
 - 2GB RAM
 - 40GB of storage (SSD or NVME)
 - Ubuntu 22.04

Установка ноды:

```
sudo apt update && sudo apt upgrade -y
```

```
apt install curl iptables build-essential git wget jq make gcc nano tmux htop nvme-cli pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev -y
```

curl -fsSL https://get.docker.com | sh
sudo systemctl enable docker
sudo systemctl restart docker
sudo usermod -aG docker $USER

```
curl -fsSL https://get.docker.com | sh
sudo systemctl enable docker
sudo systemctl restart docker
sudo usermod -aG docker $USER
```

```
docker --version
```
```
apt  install docker-compose -y
```
```
#sudo chmod +x /usr/local/bin/docker-compose
```
```
docker-compose --version
```
```
git clone https://github.com/waku-org/nwaku-compose
cd nwaku-compose
```
```
cp .env.example .env
nano .env
```
Заменяем на свои значения
```
RLN_RELAY_ETH_CLIENT_ADDRESS=  # RPC Linea Sepolia
ETH_TESTNET_ACCOUNT=           #Адрес кошелька
ETH_TESTNET_KEY=               № Приватный ключ кошелька где есть тестовые linea sepolia ETH (лучше создать новый кошелек)
RLN_RELAY_CRED_PASSWORD="my_secure_keystore_password"  # Придумайте пароль

# Advanced
NWAKU_IMAGE=
NODEKEY=
DOMAIN=
EXTRA_ARGS=
RLN_RELAY_CONTRACT_ADDRESS=
```

```
git pull origin master
```

```
./register_rln.sh
```
```
docker-compose up -d
```
Отслеживать ноду можно здесь: http://localhost:3000/d/yns_4vFVk/nwaku-monitoring

localhost меняем на IP вашего сервера.
