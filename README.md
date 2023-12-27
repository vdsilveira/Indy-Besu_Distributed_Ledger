
# Indy-Besu: Distributed Ledger

Este repositório é uma adaptação do repositório Indy-besu configurado para a distribuição dos Nodes em maquinas virtuais

- [Repositório Original](https://github.com/DSRCorporation/indy-node/tree/indy-besu/indy-besu)

# ⚙️ Configurações 
## 1 - Baixe os arquivos das pastas vm  

 - ### Em sua vm-01 execute o seguinte comando:
```bash
git clone --single-branch --branch main --depth 1 https://github.com/vdsilveira/Indy-Besu_Distributed_Ledger.git
mv Indy-Besu_Distributed_Ledger/vm-01/indy-besu /caminho/do/seu/destino
rm -rf Indy-Besu_Distributed_Ledger

```
*obs: Indique o caminho da pasta de destino em sua VM* 

- ### Em sua vm-02 execute o seguinte comando:
```bash
git clone --single-branch --branch main --depth 1 https://github.com/vdsilveira/Indy-Besu_Distributed_Ledger.git
mv Indy-Besu_Distributed_Ledger/vm-02/indy-besu /caminho/do/seu/destino
rm -rf Indy-Besu_Distributed_Ledger

```
*obs: Indique o caminho da pasta de destino em sua VM* 

- ### Em sua vm-03 execute o seguinte comando:
```bash
git clone --single-branch --branch main --depth 1 https://github.com/vdsilveira/Indy-Besu_Distributed_Ledger.git
mv Indy-Besu_Distributed_Ledger/vm-03/indy-besu /caminho/do/seu/destino
rm -rf Indy-Besu_Distributed_Ledger

```
*obs: Indique o caminho da pasta de destino em sua VM* 

- ### Em sua vm-04 execute o seguinte comando:
```bash
git clone --single-branch --branch main --depth 1 https://github.com/vdsilveira/Indy-Besu_Distributed_Ledger.git
mv Indy-Besu_Distributed_Ledger/vm-02/indy-besu /caminho/do/seu/destino
rm -rf Indy-Besu_Distributed_Ledger

```
*obs: Indique o caminho da pasta de destino em sua VM* 


## 2 - Dentro de cada VM configure os Nodes  

*obs: Estes passo devem ser feitos em ada VM*

## 🗂️ Pastas:

### 📝 Edit o arquivo .env 

- 1-Altere o Node Number

- 2- Altere os IPs dos Hosts com os IPs de suas respectivamas Maquinas virtuais

    #HOSTS
    NODE_NUMBER=1
    HOST1=127.0.0.1
    HOST2=127.0.0.1
    HOST3=127.0.0.1
    HOST4=127.0.0.1

### 📝 Detro de ./network/config/besu/  altere o arquivo .env 

- 1-Comando:

```bash
cd ./network/config/besu/
sudo nano .env
```

- 2- Altere o caminho para o arquivo "log-config.xml"


    LOG4J_CONFIGURATION_FILE=/coloque/o/seu/caminho/indy-besu/network/config/besu/log-config.xml

##  3 - Rodando os containers

- Iniciando os containers:

```bash
  docker-compose up

```

*Obs: Inicie o Node 1 primeiro somente depois os demais Nodes, eles devem sincronizar altomaticamente e após alguns minutos devem gerar blocos*

##  3 - Derrubadno os containers

- Para derrubar os containers:

```bash
 docker-compose down

```
