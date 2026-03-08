# Gerenciamento de Pacotes com RPM

O **RPM (Red Hat Package Manager)** é o sistema de gerenciamento de pacotes utilizado em distribuições baseadas em Red Hat.

Ele permite **instalar, atualizar, remover e consultar pacotes** no sistema.

Distribuições que utilizam RPM:

- RHEL
- CentOS
- Rocky Linux
- Fedora

---

# Baixando um pacote

Um pacote `.rpm` pode ser baixado diretamente da internet utilizando o comando `wget`.

Exemplo:

```bash
wget https://exemplo.com/pacote.rpm
```

O `wget` é um utilitário utilizado para **baixar arquivos da internet via terminal**.

---

# Instalando um pacote

Para instalar um pacote `.rpm` manualmente:

```bash
sudo rpm -i pacote.rpm
```

Opção utilizada:

```
-i
```

Significado:

```
install
```

Exemplo:

```bash
sudo rpm -i google-chrome.rpm
```

---

# Atualizando um pacote

Para atualizar um pacote:

```bash
sudo rpm -U pacote.rpm
```

Opção:

```
-U
```

Significado:

```
upgrade
```

Se o pacote não estiver instalado, ele será instalado automaticamente.

Outra opção relacionada:

```
-F
```

Significado:

```
freshen
```

Atualiza o pacote **somente se ele já estiver instalado**.

---

# Removendo um pacote

Para remover um pacote instalado:

```bash
sudo rpm -e nome-do-pacote
```

Opção utilizada:

```
-e
```

Significado:

```
erase
```

Exemplo:

```bash
sudo rpm -e httpd
```

---

# Consultando pacotes

O RPM também permite consultar informações sobre pacotes instalados.

Verificar se um pacote está instalado:

```bash
rpm -q nome-do-pacote
```

Opção:

```
-q
```

Significado:

```
query
```

---

# Informações de um pacote instalado

Para ver informações detalhadas de um pacote:

```bash
rpm -qi nome-do-pacote
```

---

# Listar arquivos de um pacote

Para listar todos os arquivos que pertencem a um pacote instalado:

```bash
rpm -ql nome-do-pacote
```

---

# Descobrir a qual pacote pertence um arquivo

```bash
rpm -qf /caminho/do/arquivo
```

Exemplo:

```bash
rpm -qf /usr/bin/vim
```

---

# Consultar pacote sem instalar

Também é possível consultar informações de um pacote `.rpm` antes da instalação.

Informações do pacote:

```bash
rpm -qpi pacote.rpm
```

Listar arquivos do pacote:

```bash
rpm -qpl pacote.rpm
```

Nesse caso:

```
-p
```

Significa que a consulta será feita diretamente no **arquivo do pacote**, e não em um pacote instalado no sistema.
