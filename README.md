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
   medusa -h (IP) -u msfadmin -P /usr/share/wordlists/rockyou.txt -M ftp

2. **Automação em Formulário Web (DVWA)**

   Teste de login com Medusa ou Hydra.

4. **Password Spraying em SMB com Enumeração**
   ```bash
   enum4linux -a (IP)
   medusa -h (IP) -U users.txt -P password.txt -M smbnt
   ```
---

## 🔍 Resultados

Foram obtidas credenciais válidas em serviços vulneráveis.
Prints das execuções estão disponíveis na pasta /images.

---

## 🛡️ Recomendações de Mitigação

Implementar políticas de senha forte.
Configurar bloqueio após tentativas falhas.
Utilizar autenticação multifator (MFA).
Monitorar logs e alertas de tentativas suspeitas.
