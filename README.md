# 🔐 Projeto: Testes de Força Bruta com Medusa no Kali Linux

## 📌 Descrição
Este projeto demonstra a execução de ataques de **força bruta** utilizando a ferramenta **Medusa** em um ambiente controlado com **Kali Linux** e **Metasploitable 2**. O objetivo é compreender como esses ataques funcionam, documentar os processos e propor medidas de mitigação para fortalecer a segurança.

---

## 🛠️ Ambiente Utilizado
- **VirtualBox** com duas VMs:
  - **Kali Linux** (atacante)
  - **Metasploitable 2** (alvo)
- Rede: **Host-Only**
- Ferramentas:
  - Medusa
  - Enum4linux
  - DVWA (para testes web)

---

## ✅ Cenários Testados
1. **Ataque de Força Bruta em FTP**
   ```bash
   medusa -h 192.168.56.101 -u msfadmin -P /usr/share/wordlists/rockyou.txt -M ftp
