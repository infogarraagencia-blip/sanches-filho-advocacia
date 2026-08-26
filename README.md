# Sanches & Filho Advocacia — Site institucional

Site institucional de página única (one-page), responsivo, em português.
Identidade alinhada à logo da marca: fundo **azul-marinho** (o mesmo tom da logo),
destaques em **dourado champanhe**, texto branco-platinado e tipografia serifada
elegante (Cormorant Garamond). Estrutura premium inspirada na referência (estilo
Brenda Prinsk): navegação em "pílula" flutuante, botões com gradiente dourado,
cartões de cantos arredondados, etapas numeradas, assinatura manuscrita e
marca-d'água no rodapé. A **logo oficial** aparece no cabeçalho (monograma),
no Hero (lockup completo) e no rodapé.

## Estrutura de arquivos

```
ADVOCACIA/
├── index.html            # Todo o conteúdo e a estrutura da página
├── assets/
│   ├── styles.css        # Estilos (cores, tipografia, layout, responsivo)
│   └── script.js         # Menu, FAQ, cabeçalho e animações
└── README.md             # Este arquivo
```

## Como visualizar

**Opção 1 — abrir direto no navegador (mais simples):**

```bash
open index.html
```

**Opção 2 — servidor local:**

```bash
ruby -run -e httpd . -p 8747
```

Depois acesse `http://localhost:8747`.

## Seções da página

1. **Início (Hero)** — chamada principal + logo em destaque
2. **Credenciais** — 30+ anos · 3 gerações · 2 unidades · 4 áreas
3. **Áreas de Atuação** — Cível, Trabalhista, Tributário, Penal
4. **Como funciona o atendimento** — etapas 01 a 04
5. **CTA** — "Vamos conversar sobre o seu caso?"
6. **O Escritório** — a história das gerações + assinatura
7. **Informação e Transparência** — Informado / Orientado / Acompanhado
8. **Equipe** — unidades de Dourados/MS e Fátima do Sul/MS
9. **Perguntas Frequentes**
10. **Contato final** + rodapé

## Identidade visual (variáveis em `assets/styles.css`)

| Uso                     | Variável        | Valor      |
|-------------------------|-----------------|------------|
| Fundo (azul-marinho)    | `--bg`          | `#151c27`  |
| Cartões                 | `--bg-card`     | `#1d2633`  |
| Dourado champanhe       | `--gold`        | `#e4c28a`  |
| Dourado claro           | `--gold-bright` | `#f1d8a6`  |
| Título (branco platina) | `--cream`       | `#eef1f6`  |

**Fontes:** Cormorant Garamond (títulos), Inter (texto), Great Vibes (assinatura).

## Logo e fotos

**Logo** (`assets/logo.jpg` = lockup completo; `assets/logo-lockup.jpg` = versão com
margens aparadas):
- **Cabeçalho:** monograma "SF" recortado da logo via CSS (`.brand-mark-logo img` —
  o recorte é ajustado com `left`/`top` e `width`/`height` em `assets/styles.css`).
- **Hero:** lockup completo (`.figure-logo`).
- **Rodapé:** lockup (`assets/logo-lockup.jpg`).
- **Para trocar a logo:** substitua os arquivos em `assets/` mantendo os nomes.

**Foto do Dr. Sildir** (`assets/dr-sildir.webp`): usada **apenas** na seção
**O Escritório** (`<img class="figure-photo">`). A seção **Atendimento** usa a
ilustração da balança da justiça (SVG).
- **Trocar a foto:** substitua `assets/dr-sildir.webp` (mesmo nome).
- **Ajustar o recorte:** em `assets/styles.css`, mude o `object-position` de
  `.figure-photo` (atual `56% 18%`).

**Fotos de outros advogados** (ex.: na seção Equipe): me envie que eu encaixo.

## Editar conteúdo comum (tudo em `index.html`)

- **Telefone / WhatsApp:** procure por `5567996202255` (links) — exibido como
  `(67) 9 9620-2255`.
- **Perguntas frequentes:** blocos `faq-item`.
- **Equipe:** blocos `team-member`.

## Itens opcionais a acrescentar depois

- Fotos individuais dos demais advogados (seção Equipe)
- Depoimentos reais de clientes (seção no estilo da referência)
- Redes sociais (Instagram / LinkedIn) no rodapé
- Endereços completos das unidades

## Publicação

Site estático — pode ser hospedado gratuitamente em **Netlify**, **Vercel** ou
**GitHub Pages**. Basta enviar a pasta.

---

> Conteúdo de caráter meramente informativo, em conformidade com o Código de
> Ética e Disciplina da OAB.
