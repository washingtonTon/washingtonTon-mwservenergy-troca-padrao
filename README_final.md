# mwservenergy-troca-padrao

> Página/landing para serviços de **troca de padrão elétrico** — projeto criado por **Washington / MWServEnergy**.

---

## Descrição

Site estático pensado para apresentar o serviço de troca de padrão de entrada (padrão de medição) com visual profissional, imagens de obras, e gráficos em alta definição. Este repositório contém o código fonte do site, arquivos estáticos (HTML/CSS/JS), e uma API simulada para servir imagens e gráficos HD cinematográficos.

**URL prevista (GitHub Pages):** `https://washingtonTon.github.io/mwservenergy-troca-padrao`

---

## Estrutura do repositório

```
mwservenergy-troca-padrao/
├─ index.html
├─ about.html
├─ assets/
│  ├─ images/        # fotos de obras, logos, thumbnails
│  └─ graphics/      # gráficos gerados (hd)
├─ css/
│  └─ styles.css
├─ js/
│  └─ main.js        # interações, chamadas à API de imagens/graphs
├─ api/              # (opcional) mock server / lambdas
│  └─ README.md
├─ docs/             # se usar GitHub Pages com /docs
└─ README.md         # este arquivo
```

---

## Recursos incluídos

- Landing page responsiva com seções: Hero, Serviços, Orçamento rápido, Galeria, Depoimentos e Contato.
- Galeria dinâmica que busca imagens via API local (ou estática em `/assets/images`).
- Endpoint API (mock) para imagens e gráficos HD.
- Favicons e meta tags para SEO e compartilhamento em redes.
- Exemplo de formulário de contato (integrar com Formspree, Netlify Forms, Google Forms, ou WhatsApp link direto).

---

## Como visualizar

O site pode ser aberto diretamente pelo arquivo `index.html` em qualquer navegador ou usando servidores locais como Live Server (VSCode).

Também pode ser publicado usando GitHub Pages ou outras plataformas como Netlify e Vercel.

---

## API de imagens e gráficos (exemplo)

### Endpoints propostos

- `/api/images` — retorna lista JSON de imagens da galeria.
- `/api/images/:id` — retorna imagem (ou URL) em alta resolução.
- `/api/graphs` — retorna metadados dos gráficos HD disponíveis.
- `/api/graphs/:id` — retorna imagem do gráfico em alta resolução.

### Exemplo de resposta (`/api/images`)

```json
[
  {"id":"obra-01","title":"Troca de padrão - condomínio","thumb":"/assets/images/obra-01-thumb.jpg","hd":"/assets/images/obra-01-hd.jpg"},
  {"id":"obra-02","title":"Instalação caixa nova","thumb":"/assets/images/obra-02-thumb.jpg","hd":"/assets/images/obra-02-hd.jpg"}
]
```

### Trecho JS para buscar imagens

```js
fetch('/api/images')
  .then(res => res.json())
  .then(list => {
    const galeria = document.querySelector('#galeria');
    list.forEach(item => {
      const img = document.createElement('img');
      img.src = item.thumb;
      img.alt = item.title;
      img.dataset.hd = item.hd;
      galeria.appendChild(img);
    });
  });
```

---

## SEO, performance e imagens HD

- Imagens otimizadas em formatos modernos (WebP/AVIF) quando possível.
- Uso de `loading="lazy"` para carregar imagens da galeria.
- `manifest.json` e meta tags para SEO e redes sociais.

---

## Deploy automático

- **GitHub Pages** — gratuito e integrado ao repositório.
- **Netlify** — deploy contínuo conectado ao branch principal.
- **Vercel** — suporte rápido a sites estáticos.

---

## Personalização rápida

- Texto de destaque e preços em `index.html`.
- Fotos em `assets/images/` (preferencialmente imagens reais de serviços).
- Botões de contato com link direto para WhatsApp: `https://wa.me/5511920113230`.

---

## Contato profissional

- **Washington / MWServEnergy**
- WhatsApp profissional: **(11) 92011-3230**
- Email: `washington_caio@hotmail.com`

---

## Boas práticas

1. Manter versão otimizada das imagens em `assets/images/` e originais em `assets/source/`.
2. Mensagens de atualização claras para organização do histórico.
3. Testes frequentes no celular para responsividade.
4. Inclusão de formulário simples que envie mensagem direta para WhatsApp.

---

## Licença

Licença MIT — livre para adaptação e distribuição.
