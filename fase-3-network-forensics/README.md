# Fase 3 - Network Forensics & AWS Fundamentals for Security

Esta fase é dividida em duas frentes de estudo: **Network Forensics** (análise forense de tráfego de rede) e **AWS Fundamentals for Security** (fundamentos de segurança em nuvem).

## 📡 Network Forensics

Estudo prático de captura e análise de tráfego de rede usando ferramentas como `tcpdump`, com foco em identificar padrões de comunicação, protocolos e possíveis evidências digitais.

### Programas / Laboratórios

- [x] **01 - tcpdump**: Captura e análise de pacotes (DNS, ICMP, TCP), filtros por IP/porta, geração de arquivo `.cap` para análise posterior
- [ ] **02 -** *(em breve)*
- [ ] **03 -** *(em breve)*

📁 Conteúdo do laboratório 1: [`network-forensics/01-tcpdump/`](./network-forensics/01-tcpdump/)

---

## ☁️ AWS Fundamentals for Security

Fundamentos de segurança na AWS, cobrindo desde conceitos básicos até a construção de infraestrutura de rede segura na nuvem.

### Aulas

- [ ] **Aula 1** - Conceitos básicos sobre AWS
- [ ] **Aula 2** - Primeiros passos na AWS
- [ ] **Aula 3** - Criando uma infraestrutura básica de rede e servidores na AWS
- [ ] **Aula 4** - Gerenciando acesso entre redes e servidores na AWS

📁 Conteúdo: [`aws-fundamentals-security/`](./aws-fundamentals-security/)

---

## 📂 Estrutura desta fase

```
fase-3-network-forensics/
├── README.md
├── network-forensics/
│   └── 01-tcpdump/
│       ├── captures/
│       │   └── captura.cap
│       ├── logs/
│       │   ├── dns_lookup.txt
│       │   ├── icmp_ping.txt
│       │   └── filtro_ip_porta.txt
│       └── prints/
│           ├── tcpdump_logs.png
│           ├── tcpdump_logs1.png
│           └── tcpdump_logs2.png
└── aws-fundamentals-security/
    ├── aula-1/
    ├── aula-2/
    ├── aula-3/
    └── aula-4/
```
