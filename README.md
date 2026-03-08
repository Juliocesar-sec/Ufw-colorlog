# Ufw-colorlog
# 🛡️ UFW Color Log Avançado

Um utilitário leve para transformar os logs técnicos do **UFW (Uncomplicated Firewall)** em um feed visual colorido e fácil de auditar em tempo real no seu terminal Debian/Ubuntu.

---

## ✨ O que este script faz?

O **UFW Color Log** automatiza a configuração de logs detalhados do sistema e cria um atalho (`alias`) inteligente que filtra e colore a saída do terminal de acordo com a gravidade do evento:

- 🔴 **Vermelho:** Tentativas de invasão, pacotes bloqueados (`BLOCK`, `DENIED`, `DROP`).
- 🚨 **Alerta Crítico:** Destaca tentativas em portas sensíveis (SSH, RDP, FTP, SQL).
- 🔵 **Azul:** Conexões permitidas com sucesso (`ALLOW`).
- 🟡 **Amarelo:** Identificação rápida de IPs de origem (`SRC`).
- ⚪ **Cinza:** Outros eventos informativos do Kernel.

## 🚀 Como Instalar no seu Debian/Ubuntu

Basta seguir os três passos abaixo no seu terminal:

### 1. Clonar e preparar
```bash
git clone [https://github.com/Juliocesar-sec/ufw-colorlog.git](https://github.com/SEU_USUARIO/ufw-colorlog.git)
cd ufw-colorlog
chmod +x setup_firewall.sh

2. Executar o Instalador

O script irá ativar o log full do UFW, instalar o colorizador ccze e configurar o atalho no seu .bashrc.
Bash

./setup_firewall.sh

3. Ativar as alterações

Para que o comando funcione imediatamente no terminal atual, rode:
Bash

source ~/.bashrc

🛠️ Como Usar

Após a instalação, você não precisa mais de comandos longos. Basta digitar:
Bash

ufw-colorlog

Nota: Como o script lê logs do Kernel (journalctl -k), ele solicitará sua senha de sudo para garantir a segurança dos dados.
📋 Requisitos do Sistema

    Sistema Operacional: Debian 12+, Ubuntu 22.04+ (ou derivados).

    Firewall: UFW instalado e habilitado (sudo ufw enable).

    Dependências: ccze (instalado automaticamente pelo script) e awk.

🤝 Contribuindo

Sinta-se à vontade para abrir uma Issue ou enviar um Pull Request se desejar:

    Adicionar mais portas à lista de monitoramento crítico.

    Melhorar a expressão regular do AWK para capturar mais detalhes.

    Adaptar para outros firewalls como iptables puro ou firewalld.

📄 Licença

Este projeto está sob a licença MIT. Consulte o arquivo LICENSE para mais detalhes.

Desenvolvido para facilitar a vida de SysAdmins e entusiastas de segurança Linux. 🐧
