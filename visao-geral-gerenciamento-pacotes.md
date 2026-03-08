# Visão Geral do Gerenciamento de Pacotes

O gerenciamento de pacotes é o sistema utilizado pelas distribuições Linux para **instalar, atualizar, remover e gerenciar softwares** no sistema.

Esse modelo facilita a administração do sistema operacional e permite que softwares sejam instalados de forma rápida e segura.

---

# Windows vs Linux

## Windows

No Windows, os programas normalmente são distribuídos como **arquivos executáveis**.

Os formatos mais comuns são:

```
.exe
.msi
```

Para instalar um programa geralmente é necessário:

1. Procurar o software na internet
2. Baixar o instalador
3. Executar o arquivo de instalação

Nesse modelo, o gerenciamento de dependências e atualizações costuma ser feito individualmente por cada programa.

---

## Linux

No Linux, os softwares são distribuídos em **pacotes gerenciados pelo sistema operacional**.

Esses pacotes são instalados através de **gerenciadores de pacotes**, que automatizam tarefas como:

- instalação de software
- atualização
- remoção
- gerenciamento de dependências

---

# Formatos de Pacotes

O formato dos pacotes pode variar dependendo da distribuição Linux.

## Distribuições baseadas em Red Hat

Distribuições dessa família utilizam pacotes no formato:

```
.rpm
```

Exemplos de distribuições:

- RHEL
- CentOS
- Rocky Linux
- Fedora

---

## Distribuições baseadas em Debian

Distribuições dessa família utilizam pacotes no formato:

```
.deb
```

Exemplos de distribuições:

- Debian
- Ubuntu
- Linux Mint

---

## Pacotes compactados

Alguns softwares também podem ser distribuídos como arquivos compactados, normalmente no formato:

```
.tar.gz
```

Nesse caso, a instalação pode exigir **compilação manual ou execução de scripts de instalação**.

---

# Repositórios

As distribuições Linux utilizam **repositórios de software**.

Repositórios são servidores que armazenam pacotes oficiais mantidos pela distribuição.

Isso permite instalar softwares diretamente pelo terminal sem precisar procurar instaladores na internet.

Exemplo de instalação de software.

Distribuições baseadas em Debian:

```bash
sudo apt install nginx
```

Distribuições baseadas em Red Hat:

```bash
sudo dnf install nginx
```

O gerenciador de pacotes automaticamente:

- baixa o pacote
- resolve dependências
- instala o software
- registra o pacote no sistema
