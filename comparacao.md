# Comparação de Gerenciadores de Pacotes

Diferentes distribuições Linux utilizam sistemas de gerenciamento de pacotes distintos.

Apesar das diferenças, todos possuem o mesmo objetivo:

- instalar software
- atualizar programas
- remover pacotes
- gerenciar dependências

---

# RPM vs DNF/YUM

O **RPM** é o sistema de gerenciamento de pacotes de baixo nível utilizado em distribuições baseadas em Red Hat.

Ele trabalha diretamente com arquivos `.rpm`.

Exemplo:

```bash
sudo rpm -i pacote.rpm
```

Porém o RPM **não resolve dependências automaticamente**.

Por isso ferramentas como **DNF** e **YUM** foram criadas.

Essas ferramentas funcionam como **camadas superiores**, facilitando o gerenciamento de software.

Exemplo com DNF:

```bash
sudo dnf install nginx
```

Nesse caso o sistema:

- localiza o pacote
- baixa dependências
- instala tudo automaticamente

---

# APT vs DNF

APT e DNF são gerenciadores de pacotes modernos utilizados em distribuições diferentes.

| Característica | APT | DNF |
|---|---|---|
Distribuições | Debian, Ubuntu | Fedora, RHEL, Rocky Linux |
Formato de pacote | `.deb` | `.rpm` |
Gerenciamento de dependências | automático | automático |
Repositórios | sim | sim |
Atualização do sistema | `apt upgrade` | `dnf update` |

---

# Instalação de software

Exemplo de instalação de um software em diferentes sistemas.

## Debian / Ubuntu

```bash
sudo apt install nginx
```

## Fedora / RHEL / Rocky Linux

```bash
sudo dnf install nginx
```

Ambos os comandos:

- localizam o pacote no repositório
- baixam dependências
- instalam o software
- registram o pacote no sistema

---

# Estrutura dos sistemas de pacotes

Distribuições Linux normalmente seguem esta estrutura:

```
Pacote (rpm ou deb)
        ↓
Gerenciador de baixo nível (rpm / dpkg)
        ↓
Gerenciador de alto nível (dnf / apt)
        ↓
Repositórios de software
```

Essa arquitetura permite que o sistema gerencie softwares de forma **segura, organizada e automatizada**.

---

# Conclusão

O gerenciamento de pacotes é uma das principais características que diferenciam as distribuições Linux de outros sistemas operacionais.

Ferramentas como:

- **APT**
- **DNF**
- **YUM**
- **RPM**

permitem que administradores de sistemas instalem e mantenham softwares de forma eficiente.

Esse modelo facilita a manutenção do sistema e melhora a segurança, já que atualizações podem ser aplicadas rapidamente através dos repositórios oficiais.
