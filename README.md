# O Que é Espírito? — GitHub Pages

Site estático hospedado no GitHub Pages que exibe um PDF diretamente no navegador, com rastreamento via **Google Analytics 4**.

## 🚀 Como configurar

### 1. Adicionar o PDF ao repositório

Coloque o arquivo PDF na **raiz do repositório** com o nome exato `oqueespirito.pdf`:

```
oqueespirito/
├── index.html
├── oqueespirito.pdf   ← adicione aqui
├── .nojekyll
└── README.md
```

### 2. Configurar o Google Analytics 4

1. Acesse [analytics.google.com](https://analytics.google.com) e crie uma conta / propriedade GA4.
2. Copie o **Measurement ID** (formato `G-XXXXXXXXXX`).
3. No arquivo `index.html`, substitua **ambas** as ocorrências de `G-XXXXXXXXXX` pelo seu ID real:

```html
<!-- linha 11 -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-SEU-ID-AQUI"></script>
<!-- linha 16 -->
gtag('config', 'G-SEU-ID-AQUI');
```

### 3. Ativar o GitHub Pages

1. Vá em **Settings → Pages** no repositório.
2. Em **Source**, selecione a branch `main` (ou `master`) e a pasta `/ (root)`.
3. Clique em **Save**.

O site ficará disponível em `https://samuelmattos.github.io/oqueespirito/`.

## 📊 O que é rastreado

- Pageviews automáticos de todos os visitantes.
- Evento personalizado `view_document` disparado a cada abertura do PDF.

## 🛠 Tecnologias

- HTML5 puro (sem dependências)
- Google Analytics 4 (GA4)
- GitHub Pages
