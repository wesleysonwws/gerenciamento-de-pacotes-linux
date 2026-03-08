# Gerenciamento de Pacotes com YUM e DNF

O **YUM** e o **DNF** são gerenciadores de pacotes utilizados em distribuições Linux baseadas em Red Hat.

Eles funcionam como uma camada acima do **RPM**, facilitando o gerenciamento de software.

Essas ferramentas são responsáveis por:

- instalar pacotes
- remover pacotes
- atualizar o sistema
- resolver dependências automaticamente
- acessar repositórios de software

Distribuições que utilizam YUM ou DNF:

- RHEL
- CentOS
- Rocky Linux
- Fedora

---

# Diferença entre YUM e DNF

O **YUM (Yellowdog Updater Modified)** foi durante muitos anos o gerenciador padrão dessas distribuições.

Com o tempo, ele foi substituído pelo **DNF (Dandified YUM)**, que é mais rápido e possui melhor gerenciamento de dependências.

Hoje:

- **DNF** é utilizado nas versões modernas
- **YUM** ainda existe por compatibilidade

---

# Atualizar a lista de pacotes

Antes de instalar novos programas, é recomendado atualizar os metadados dos repositórios.

Com DNF:

```bash
sudo dnf check-update
```

Com YUM:

```bash
sudo yum check-update
```

---

# Instalar um pacote

Para instalar um software:

Com DNF:

```bash
sudo dnf install nome-do-pacote
```

Com YUM:

```bash
sudo yum install nome-do-pacote
```

Exemplo:

```bash
sudo dnf install nginx
```

Durante a instalação, o gerenciador de pacotes automaticamente:

- baixa o pacote
- resolve dependências
- instala os arquivos necessários
- registra o pacote no sistema

---

# Remover um pacote

Para remover um software do sistema:

Com DNF:

```bash
sudo dnf remove nome-do-pacote
```

Com YUM:

```bash
sudo yum remove nome-do-pacote
```

Exemplo:

```bash
sudo dnf remove nginx
```

---

# Atualizar pacotes

Para atualizar todos os pacotes instalados no sistema:

Com DNF:

```bash
sudo dnf update
```

Com YUM:

```bash
sudo yum update
```

Esse comando verifica os repositórios e instala versões mais recentes dos pacotes.

---

# Procurar pacotes

Para pesquisar softwares disponíveis nos repositórios:

Com DNF:

```bash
dnf search palavra-chave
```

Exemplo:

```bash
dnf search nginx
```

---

# Ver informações de um pacote

Para visualizar detalhes de um pacote disponível:

```bash
dnf info nome-do-pacote
```

Exemplo:

```bash
dnf info nginx
```

As informações exibidas podem incluir:

- versão
- tamanho
- descrição
- repositório de origem

---

# Listar pacotes instalados

Para listar todos os pacotes instalados no sistema:

```bash
dnf list installed
```

---

# Repositórios

Os repositórios são servidores que armazenam pacotes de software utilizados pela distribuição.

Esses repositórios permitem instalar programas diretamente do terminal sem precisar baixar arquivos manualmente.

Listar repositórios configurados:

```bash
dnf repolist
```

Os arquivos de configuração dos repositórios geralmente ficam em:

```
/etc/yum.repos.d/
```
