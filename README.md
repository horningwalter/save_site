# SAVE · Hospital Veterinário

Site institucional da SAVE (Serviço de Atendimento Veterinário Especializado), em Curitiba. Apresenta a mudança já realizada para a nova unidade em Santa Quitéria e o novo momento como Hospital Veterinário.

## Stack

- [Astro](https://astro.build) 7 (site estático, sem framework de UI)
- CSS próprio em `src/styles/global.css` (design tokens no `:root`)
- Tailwind disponível via Vite, mas a página é estilizada com CSS autoral

## Requisitos

Node.js **22.23.4** ou superior.

## Comandos

| Comando           | Ação                                          |
| :---------------- | :-------------------------------------------- |
| `npm install`     | Instala as dependências                       |
| `npm run dev`     | Servidor local em `localhost:4321`            |
| `npm run build`   | Gera o site estático em `./dist/`             |
| `npm run preview` | Pré-visualiza o build local                   |

## Estrutura

```text
/
├── public/
│   ├── media/            # fotos e renders (WebP/JPG)
│   └── favicon.*
├── src/
│   ├── components/       # Header, Hero, Facts, NovoHospital, Estrutura,
│   │                     # Servicos, Historia, Contato, Footer, WhatsAppFloat
│   ├── layouts/Layout.astro
│   ├── pages/index.astro
│   └── styles/global.css # tokens, tipografia, grid, responsivo
└── astro.config.mjs
```

Seções da página, na ordem: `#inicio`, faixa de dados, `#novo-hospital`, `#estrutura`, `#servicos`, `#historia`, `#contato`.

## Direção de arte

- **Cores:** vermelho institucional `#970014`, vinho `#570008`, marfim `#f8f3ed`, superfície `#fffcf8`.
- **Tipografia:** Manrope (títulos e UI), Inter (texto), Cormorant Garamond itálico (expressões emocionais).
- **Composição:** hero e seção 01 em spreads que sangram até a borda; galeria da estrutura em sequência editorial com proporções variadas (16:10, 4:5, 16:9, 21:9).

## Deploy

O site é estático e pode ser publicado em qualquer host (Vercel, Netlify, Cloudflare Pages). Build: `npm run build`, saída: `dist/`.

Variáveis de ambiente:

| Variável            | Efeito                                                                 |
| :------------------ | :--------------------------------------------------------------------- |
| `PUBLIC_NOINDEX`    | `false` libera indexação. Por padrão a proposta fica como `noindex`.    |
| `PUBLIC_SITE_URL`   | Domínio final (ex.: `https://save.com.br`) para URLs absolutas de SEO.  |

Em previews da Vercel, `VERCEL_URL` é usada automaticamente para o `og:image`.

## Conteúdo

Os textos seguem o material aprovado da SAVE. Dados ainda pendentes de confirmação (horário 24h, autorização dos renders) não são afirmados no site.

---

Site por [Facilia](https://facilia.ia.br).
