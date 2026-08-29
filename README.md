# ⚡ DotCast — Digital Signage System

<p align="center">
  <img width="278" height="93" alt="logo" src="https://github.com/user-attachments/assets/1725520f-4e98-4632-a91d-38b8030194af" />
  <br>
  <strong>Sistema Autónomo de Transmissão Multimédia em Rede Local</strong>
  <br>
  <em>Desenvolvido para ecrãs de montra e loja na Dotbright</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Vers%C3%A3o-1.3.3-FF6B00?style=for-the-badge" alt="Versão">
  <img src="https://img.shields.io/badge/Plataforma-Windows%20%7C%20Android%20TV-121318?style=for-the-badge&logo=windows" alt="Plataformas">
  <img src="https://img.shields.io/badge/Tecnologia-Node.js%20%26%20WebSockets-10B981?style=for-the-badge" alt="Tech">
</p>

---

## 📌 Sobre o Projeto

O **DotCast** é uma solução completa de *Digital Signage* (sinalética digital) desenhada para correr de forma autónoma num computador Windows e transmitir imagens e vídeos promocionais para uma **Xiaomi Box (Android TV)** ligada a um televisor na loja, através da rede local (Wi-Fi/Ethernet), sem depender de serviços externos ou custos de subscrição na cloud.

---

## 🚀 Funcionalidades Principais

* **Interface Cyber-Tech Dark & Orange:** Painel de gestão moderno com estética de laboratório de reparações electrónicas, fundo de circuito animado e cartões translúcidos (*glassmorphism*).
* **Arranque Silencioso (Zero CMD):** Execução em segundo plano como aplicação nativa de interface gráfica, sem abrir terminais ou janelas pretas no ecrã.
* **Upload Rápido com Drag-and-Drop:** Suporte para imagens (`.jpg`, `.png`, `.webp`, `.gif`) e vídeos (`.mp4`, `.webm`) até 500 MB com cálculo de progresso em tempo real.
* **Sincronização Imediata (WebSockets):** Qualquer alteração feita no painel de controlo reflete-se na TV instantaneamente sem necessidade de atualizar a página (`F5`).
* **Double-Buffering no Player:** Alternância suave entre conteúdos com transição *crossfade* sem ecrãs pretos ou quebras de carregamento.
* **Privacidade Visual na Loja:** O ecrã de standby da TV não expõe endereços IP aos clientes por defeito (Modo Debug acessível apenas via tecla `D`).
* **Auto-Diagnóstico (System Doctor):** Deteção inteligente do IPv4 físico, teste de portas locais e verificação de permissões de disco.
* **Auto-Atualizador Integrado:** Verificação de novas versões diretamente através das Releases do GitHub.

---

## 🛠️ Tecnologias Utilizadas

* **Backend:** Node.js, Express, Socket.io, Multer
* **Frontend:** HTML5, CSS3 Glassmorphism, JavaScript ES6+
* **Compilação & Proteção:** `@yao-pkg/pkg`, `javascript-obfuscator`, PE Subsystem Patching
* **Resiliência Android TV:** Double-Buffering DOM Layering, Auto-Garbage Collection de Vídeo

---

## 📦 Estrutura do Projeto

```text
DotCast/
├── server/               # Lógica de servidor Express, sockets e diagnósticos
├── public/
│   ├── admin/            # Interface de Gestão (Dark Mode Dotbright)
│   └── player/           # Interface de Exibição da TV (100% Fullscreen)
├── data/                 # Base de dados JSON persistente (playlist.json)
├── uploads/              # Armazenamento físico de ficheiros multimédia
├── scripts/              # Scripts de Firewall e Patch de binários
├── build-portable.bat    # Gerador da versão executável autónoma (.exe)
└── package.json

```

---

## 💻 Como Utilizar

### 1. No PC da Loja

* Executa o ficheiro **`DotCast.exe`** (ou `Iniciar DotCast.vbs`).
* O painel de administração abre automaticamente no browser em `http://127.0.0.1:3000/admin`.
* Arrasta imagens ou vídeos para a zona de upload e organiza a ordem de exibição.

### 2. Na Xiaomi Box / Smart TV

* Abre o navegador na TV (ex: **TV Bro** ou **Fully Kiosk Browser**).
* Acede ao endereço apresentado no painel (ex: `http://192.168.1.X:3000/player`) ou faz o scan do código QR no botão **Conectar TV (QR)**.
* Coloca o navegador em modo de ecrã inteiro.

---

## 👨‍💻 Créditos & Desenvolvimento

* **Autor / Desenvolvedor:** [Miguel](https://www.google.com/search?q=https://github.com/Miguel7258)
* **Desenvolvimento & Engenharia:** Parceria entre **Miguel** e **Antigravity 2.0**
* **Empresa / Marca:** [Dotbright](https://www.dotbright.pt) — Reparação Especializada de Smartphones e Computadores

---

## 📄 Licença

Distribuído sob licença proprietária para uso na infraestrutura interna da **Dotbright**. Todos os direitos reservados.
