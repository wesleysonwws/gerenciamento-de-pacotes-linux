# Gerenciamento de Pacotes com APT

O **APT (Advanced Package Tool)** é o gerenciador de pacotes utilizado em distribuições Linux baseadas em Debian.

Ele permite instalar, atualizar, remover e pesquisar softwares de forma simples utilizando repositórios oficiais.

Distribuições que utilizam APT:

- Debian
- Ubuntu
- Linux Mint
- Pop!_OS
- Kali Linux

O APT trabalha com pacotes no formato:

```
.deb
```

---

# Atualizar lista de pacotes

Antes de instalar novos softwares, é recomendado atualizar a lista de pacotes disponíveis nos repositórios.

```bash
sudo apt update
```

Esse comando sincroniza o sistema com os repositórios configurados.

---

# Atualizar pacotes instalados

Para atualizar todos os pacotes instalados no sistema:

```bash
sudo apt upgrade
```

Esse comando instala as versões mais recentes disponíveis.

Para uma atualização mais completa:

```bash
sudo apt full-upgrade
```

Esse modo permite remover ou substituir pacotes se necessário.

---

# Instalar um pacote

Para instalar um software:

```bash
sudo apt install nome-do-pacote
```

Exemplo:

```bash
sudo apt install nginx
```

Durante a instalação o APT automaticamente:

- baixa o pacote
- resolve dependências
- instala o software
- registra o pacote no sistema

---

# Remover um pacote

Para remover um pacote instalado:

```bash
sudo apt remove nome-do-pacote
```

Exemplo:

```bash
sudo apt remove nginx
```

Esse comando remove o programa, mas mantém arquivos de configuração.

---

# Remover completamente um pacote

Para remover o pacote **e seus arquivos de configuração**:

```bash
sudo apt purge nome-do-pacote
```

Exemplo:

```bash
sudo apt purge nginx
```

---

# Limpar pacotes desnecessários

Depois de remover programas, algumas dependências podem permanecer instaladas.

Para removê-las:

```bash
sudo apt autoremove
```

Esse comando remove pacotes que não são mais necessários.

---

# Procurar pacotes

Para pesquisar softwares disponíveis:

```bash
apt search palavra-chave
```

Exemplo:

```bash
apt search nginx
```

---

# Ver informações de um pacote

Para visualizar detalhes de um pacote:

```bash
apt show nome-do-pacote
```

Exemplo:

```bash
apt show nginx
```

As informações podem incluir:

- versão
- tamanho
- descrição
- dependências
- repositório de origem

---

# Listar pacotes instalados

Para listar todos os pacotes instalados:

```bash
apt list --installed
```

---

# Repositórios

Os repositórios são servidores que armazenam os pacotes utilizados pela distribuição.

Eles permitem instalar e atualizar softwares diretamente pelo terminal.

O arquivo principal de repositórios fica em:

```
/etc/apt/sources.list
```

Arquivos adicionais podem estar em:

```
/etc/apt/sources.list.d/
```
