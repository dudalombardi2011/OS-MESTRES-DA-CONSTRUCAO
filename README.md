# 🏗️ MESTRES DA CONSTRUÇÃO - NPCARQ 2026

O **Mestres da Construção** é uma plataforma de ranking em tempo real desenvolvida em low code para a capacitação de trainees do NPCARQ em 2026 da empresa junior CimatecJr. O sistema monitora o progresso dos participantes através da contagem de "tijolinhos", exibindo os líderes em um pódio dinâmico e uma lista detalhada de todos os competidores.

## 🚀 Funcionalidades

- **Ranking em Tempo Real:** Integração direta com Google Sheets para atualização instantânea de pontos.
- **Pódio Dinâmico:** Destaque visual para os 3 primeiros colocados com efeitos de animação.
- **Tratamento Inteligente de Imagens:**
  - Conversão automática de links do Google Drive.
  - **Image Proxy:** Servidor interno que contorna restrições de exibição (embed) do Google Drive.
  - **Fallback de Avatares:** Geração automática de avatares com iniciais caso a imagem falhe.
- **Interface Futurista:** Design "Glassmorphism" com paleta de cores vibrantes e animações suaves via Framer Motion.
- **Responsividade Total:** Otimizado para visualização em desktops, tablets e dispositivos móveis.

## 🛠️ Tecnologias Utilizadas

- **Frontend:**
  - [React 18](https://reactjs.org/)
  - [Vite](https://vitejs.dev/)
  - [Tailwind CSS](https://tailwindcss.com/)
  - [Motion (Framer Motion)](https://motion.dev/)
  - [Lucide React](https://lucide.dev/) (Ícones)
- **Backend (Proxy):**
  - [Express](https://expressjs.com/) (Node.js)
- **Dados:**
  - [Google Apps Script](https://developers.google.com/apps-script) (API de integração com Planilhas)

## 📁 Estrutura do Projeto

```text
├── src/
│   ├── components/       # Componentes reutilizáveis
│   ├── services/
│   │   └── dataService.ts # Lógica de busca e tratamento de dados
│   ├── App.tsx           # Componente principal e UI
│   ├── main.tsx          # Ponto de entrada React
│   └── index.css         # Estilização global e temas Tailwind
├── server.ts             # Servidor Express com Proxy de Imagens
├── index.html            # Template HTML principal
└── package.json          # Dependências e scripts
```

## ⚙️ Configuração Técnica

### Integração com Google Sheets
O projeto consome dados de um Web App do Google Apps Script. A estrutura esperada dos dados (JSON) é:

```json
[
  {
    "name": "Nome do Trainee",
    "tijolinhos": 150,
    "imageUrl": "https://drive.google.com/..."
  }
]
```

Esta rota processa a requisição no servidor e entrega o buffer da imagem diretamente ao navegador.

## ✒️ Créditos

Desenvolvido para **CimatecJr • NPCARQ • 2026**.
