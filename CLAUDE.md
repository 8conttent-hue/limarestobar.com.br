# CLAUDE.md — LIMARESTOBAR

Site gerado pelo **SF (Site Factory)** em 15/04/2026.

## Contexto do Site

**Nome:** LIMARESTOBAR
**Nicho:** Gastronomia
**Keywords:** O Restaurante O Chef Marco Espinoza 33 anos ainda vai dar muito
**Paleta de cores:** forest | **Fonte:** montserrat

O Restaurante O Chef Marco Espinoza, 33 anos, ainda vai dar muito o que falar. No comando de um dos mais conceituados restaurantes de Brasília, o contemporâneo Taypá Sabores Del Peru, o peruano desembarcou recentemente no Rio de Janeiro para comandar o Lima RestoBar, mix de restaurante e bar, na charmosa Rua Visconde de Caravelas, em Botafogo. O restaurante ocupa uma casa de dois andares com 120m² e decoração no estilo contemporâneo. Materiais antigos como a madeira de demolição e o ferro se destacam na decoração do local. Duas grandes luminárias chamam a atenção logo na entrada. O projeto foi assinado pela arquiteta Teresa Guerreiro, cuja inspiração veio da própria apresentação dos pratos do Lima: jovem como o Chef e moderna como o proposta.



## Componentes visuais usados

| Seção | Variante |
|-------|----------|
| Header | Header-G |
| Hero | Hero-D |
| Features | Features-F |
| About Section | About-A |
| Posts | Posts-G |
| Footer | Footer-J |
| Página Sobre | Sobre-G |
| Página Contato | Contato-I |

## Estrutura do projeto

```
src/
  sections/        # Layout escolhido pelo SF — Header, Hero, Features, About, Posts, Footer, Sobre, Contato
  data/            # JSONs com todo o conteúdo editável
  content/blog/    # Posts em Markdown
  pages/           # Rotas Astro (index, sobre, contato, blog, privacidade, termos)
  layouts/         # BaseLayout com fonte e cores dinâmicas
  styles/          # global.css com variáveis CSS de cor
public/
  images/          # hero.jpg, about.jpg, blog/*.jpg — inseridos automaticamente via Pexels
```

## O que editar

### Textos e conteúdo
- **`src/data/home.json`** — hero (título, subtítulo, botão), features (título, items), about section (título, desc, stats), posts
- **`src/data/sobre.json`** — conteúdo completo da página Sobre (hero, texto, missão)
- **`src/data/contato.json`** — título, subtítulo, email, tempo de resposta
- **`src/data/siteConfig.json`** — nome, slug, email, redes sociais, menu

### Imagens
Imagens já estão em `public/images/` (via Pexels). Para substituir, mantenha os mesmos nomes de arquivo:
- `hero.jpg` — imagem de fundo do Hero
- `about.jpg` — imagem da seção About (home)
- `sobre.jpg` — imagem de fundo da página Sobre
- `blog/{slug}.jpg` — imagens dos posts

### Posts do blog
Arquivos em `src/content/blog/`. Ajuste o tom de voz, adicione dados específicos do nicho e personalize conforme a identidade do site.

### Cores
Variáveis em `src/styles/global.css`: `--color-primary`, `--color-accent`, `--color-dark`.

## Deploy

```bash
bun install
bun run build
# Faça upload da pasta dist/ para Netlify, Vercel ou hosting estático
```
