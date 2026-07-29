⚠️ Nota: Este repositório documenta o processo de investigação e o aprendizado obtido durante o laboratório. Informações sensíveis e respostas de desafios (flags) não são publicadas para preservar a proposta educacional.
# Network Forensics - The Miner (Wireshark)

## 📌 Objetivo

Analisar arquivos PCAP utilizando o Wireshark para identificar evidências de comunicação de rede, credenciais em texto claro, tráfego HTTP e possíveis indicadores de comprometimento (IoCs).

> Laboratório desenvolvido durante os estudos de Computação Forense e Network Forensics.

---

# 🎯 Objetivos do laboratório

- Aprender a utilizar filtros no Wireshark.
- Identificar protocolos de rede.
- Reconstruir comunicações TCP e UDP.
- Localizar credenciais transmitidas em texto claro.
- Identificar URLs e domínios presentes nas capturas.
- Diferenciar evidências reais de mensagens falsas.

---

# 🛠 Ferramentas utilizadas

- Kali Linux
- Wireshark
- Arquivos PCAP

---

# 📂 Arquivos analisados com evidências

- The_Miner_6.pcap
- The_Miner_13.cap

---

# 🔎 Metodologia

A análise foi realizada utilizando os filtros nativos do Wireshark.

Principais filtros utilizados:

```text
ftp
http
```

Também foram utilizadas as funcionalidades:

- Follow TCP Stream
- Follow UDP Stream
- Find Packet

---

# 📡 Análise FTP

Filtro utilizado:

```text
ftp
```

Foi identificado um processo de autenticação FTP contendo credenciais transmitidas em texto claro.

Fluxo observado:

```text
220 Service Ready
USER anonymous
331 Guest login ok
PASS ********
230 Login successful
```

## Aprendizados

- Funcionamento básico do protocolo FTP.
- Diferença entre requisições e respostas.
- Riscos da transmissão de credenciais sem criptografia.

---

# 🌐 Análise HTTP

Filtro utilizado:

```text
http
```

Foi identificado um download realizado através do serviço Windows Update.

Informações observadas:

- Método HTTP GET
- User-Agent Microsoft BITS
- Host Windows Update

Durante a análise foi possível compreender como uma URL completa é formada a partir de:

- Host
- Request URI

---

# 📨 Análise UDP

Utilizando:

```
Follow UDP Stream
```

Foi encontrada uma mensagem contendo um alerta sobre uma suposta vulnerabilidade do Windows.

A mensagem incentivava o usuário a acessar um determinado endereço para instalar uma atualização.

## Observação

Durante a investigação foi possível diferenciar:

- Uma mensagem contendo um endereço.
- Uma conexão HTTP efetivamente realizada.

Essa distinção é extremamente importante em análises forenses.

---

# 🧠 Conceitos aprendidos

- Display Filters
- Find Packet
- Follow TCP Stream
- Follow UDP Stream
- FTP Authentication
- HTTP GET
- Host Header
- Request URI
- User-Agent
- Indicadores de Comprometimento (IoCs)

---

# 💡 Lições Aprendidas

Este laboratório demonstrou como pequenas evidências presentes em uma captura de rede podem revelar informações importantes sobre uma comunicação.

Também reforçou a importância de validar cada evidência antes de chegar a uma conclusão, evitando assumir que um domínio citado em uma mensagem necessariamente foi acessado.

A investigação deve sempre ser baseada em evidências observáveis no tráfego de rede.

---

# 📚 Conhecimentos praticados

- Network Forensics
- Análise de Pacotes
- Wireshark
- Investigação de Incidentes
- Protocolos de Rede
- HTTP
- FTP
- UDP
- TCP

---

