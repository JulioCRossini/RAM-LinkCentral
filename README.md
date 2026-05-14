<div align="center">

<img src="RamLInkCentral.png" alt="RAM Link Central Logo" width="120" />

# RAM Link Central

**Hub de acesso rápido para ferramentas e sistemas da equipe Sistema RAM**

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![Zero Dependencies](https://img.shields.io/badge/dependências-zero-brightgreen?style=flat-square)](.)
[![Status](https://img.shields.io/badge/status-ativo-success?style=flat-square)](.)

</div>

---

## Visão Geral

O **RAM Link Central** é um painel de links interativo e visualmente rico, criado para centralizar o acesso rápido a todas as ferramentas, sistemas e serviços utilizados pela equipe [Sistema RAM](https://sistemaram.com.br). Com uma interface inspirada em **glassmorphism** e animações fluidas, substitui listas de favoritos e planilhas por um hub elegante e totalmente editável.

> Sem frameworks. Sem build steps. Abra o `index.html` e pronto.

---

## Funcionalidades

### Cards de Acesso Rápido
- Grade responsiva de 1 a 3 colunas (mobile → tablet → desktop)
- 19 cards pré-configurados cobrindo sistemas internos, ferramentas de nuvem, consultas fiscais e muito mais
- Animação de entrada escalonada e efeito de inclinação 3D ao passar o mouse
- Ripple animado ao clicar no botão de acesso

### Busca com Liquid Glass
- Barra de pesquisa expansível com estética glassmórfica
- Ícone de lupa com animação de burst ao ativar
- Filtragem em tempo real por título e categoria
- Mensagem de "nenhum resultado" ao não encontrar correspondência
- Fecha com `Esc` ou botão X

### Editor de Cards
- Modal para criar e editar cards diretamente na interface
- Upload de avatar com redimensionamento automático (máx. 320 px, JPEG 0.82)
- Preview do avatar com fallback para iniciais
- Campos: iniciais, título, subtítulo e URL

### Persistência e Exportação
- Cards salvos automaticamente no `localStorage`
- Cards personalizados mantidos entre sessões
- Botão de exportação gera um `data.json` atualizado para backup ou deploy

### Visual e Animações
| Elemento | Descrição |
|---|---|
| Partículas | Canvas animado com partículas flutuantes responsivas |
| Blobs | 3 gradientes de fundo com movimento senoidal |
| Grid | Overlay sutil de grade azul 64×64 px |
| Título shimmer | Efeito de gradiente animado no heading principal |
| Glassmorphism | `backdrop-filter: blur` em modais, busca e cards |

---

## Tecnologias

| Camada | Tecnologia |
|---|---|
| Estrutura | HTML5 semântico |
| Estilo | Tailwind CSS (CDN) + CSS customizado |
| Lógica | Vanilla JavaScript (ES6+) |
| Renderização | Canvas API (partículas) |
| Estado | `localStorage` |
| Imagens | Base64 embutido em `data.json` |

---

## Estrutura do Projeto

```
RAM Link Central/
├── index.html          # Aplicação completa (HTML + CSS + JS)
├── data.json           # Banco de cards (títulos, URLs, imagens)
└── RamLInkCentral.png  # Logo do projeto
```

---

## Como Usar

### Localmente
```bash
# Clone o repositório
git clone https://github.com/seu-usuario/ram-link-central.git

# Abra no navegador
start index.html   # Windows
open index.html    # macOS
```

Não é necessário servidor ou dependências — funciona diretamente pelo sistema de arquivos.

### Deploy Estático
Hospede os três arquivos em qualquer serviço estático:

- **GitHub Pages** — habilite nas configurações do repositório
- **Netlify** — arraste a pasta para [app.netlify.com](https://app.netlify.com)
- **Vercel** — `vercel --prod` na raiz do projeto

---

## Cards Disponíveis

| Categoria | Ferramenta |
|---|---|
| Acesso Remoto | AnyDesk Download |
| Nuvem | Google Drive, MEGA |
| Backup | Cobian Reflector |
| Sistemas Internos | SolOp, Site Sistema RAM, RAM CRM, PontoFácil |
| Suporte | Suporte RAM, Suporte RAM Central, ChatWoot |
| Fiscal / SEFAZ | Monitor Sefaz, NFC-e, NF-e, Cadesp, Validador XML |
| Automação | ExpxAgents |

---

## Personalização

### Adicionar um card pela interface
1. Clique no tile **"+ Adicionar card"** no final da grade
2. Preencha as informações no modal
3. Clique em **Salvar** — o card aparece imediatamente

### Editar um card existente
1. Passe o mouse sobre o card
2. Clique no ícone de edição (canto superior direito)
3. Altere os campos e salve

### Editar o `data.json` diretamente
Cada card segue o formato:
```json
{
  "id": 1,
  "title": "Nome da Ferramenta",
  "subtitle": "Categoria",
  "initials": "XX",
  "url": "https://exemplo.com",
  "image": ""
}
```
Substitua `"image"` por uma string Base64 (`data:image/jpeg;base64,...`) para exibir um avatar.

### Exportar alterações
Clique no botão circular no canto inferior direito para baixar o `data.json` atualizado e substituir o arquivo do repositório.

---

## Design System

```
Fundo:       #050917  (azul quase preto)
Primário:    blue-500 → blue-700
Acento:      blue-400, blue-600
Texto:       white / rgba(white, 0.7)
Tipografia:  Inter — pesos 300 a 900
```

---

## Licença

Uso interno — Sistema RAM © 2025. Todos os direitos reservados.

---

<div align="center">
  Feito por Júlio César Rossini, com foco em produtividade para a equipe <strong>Sistema RAM</strong>
</div>
