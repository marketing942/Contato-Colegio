# Implementações de SEO — Contato Colégio CPPEM

Repositório: [`marketing942/Contato-Colegio`](https://github.com/marketing942/Contato-Colegio) · branch `seo/otimizacao-organica-20261023` (base `main`) · 23/10/2026
Relatório consolidado do ecossistema: [RELATORIO-GERAL-SEO-ECOSSISTEMA.md](RELATORIO-GERAL-SEO-ECOSSISTEMA.md)

Commits na branch `seo/otimizacao-organica-20261023`. Nada foi publicado; merge e deploy dependem de aprovação.

## Arquivos modificados

| Arquivo | Alteração | Por quê |
|---|---|---|
| index.html (`<head>`) | Title, description com Matrículas 2027 e etapas, robots, og:type/site_name/locale e JSON-LD School (endereço, telefone, e-mail, Instagram do rodapé) |  |
| robots.txt (novo) | Bloqueia `/docs/` e arquivos internos (sem Sitemap até haver domínio) |  |
| .vercelignore (novo) | `docs/seo/` |  |

## Metadados — antes × depois

Extraídos do HTML renderizado localmente (Playwright/HTTP), antes e depois.

| Campo | Antes | Depois |
|---|---|---|
| `title` | Colégio CPPEM — Fale com a gente | Colégio CPPEM em Caruaru-PE: Escola Cristã e Militarizada |
| `description` | Colégio CPPEM em Caruaru-PE: escola cristã, militarizada e preparatória. Deixe seus dados e nossa equipe fala com você. | Matrículas 2027 abertas no Colégio CPPEM, escola cristã, militarizada e preparatória em Caruaru-PE, do 1º ano do Fundamental ao 3º ano do Médio. Fale conosco. |
| `canonical` | — | https://contato.colegio.cppem.com.br/ |
| `robots` | — | index, follow, max-image-preview:large |
| `og:image` | — | https://contato.colegio.cppem.com.br/public/img/og-colegio-cppem.jpg |
| `og:url` | — | https://contato.colegio.cppem.com.br/ |
| `og:type` | — | website |
| `og:site_name` | — | Colégio CPPEM |
| `og:locale` | — | pt_BR |
| JSON-LD |  | School |

## Dados estruturados

Só tipos aplicáveis e só com dados que a página mostra. Nada de avaliações,
preços inventados, prêmios ou credenciais. Sem `FAQPage` (o resultado de FAQ
foi restrito a sites de governo e saúde em 2023 — [Google — Mudanças nos resultados de FAQ/HowTo (2023)](https://developers.google.com/search/blog/2023/08/howto-faq-changes) — e o
changelog da documentação registra a descontinuação em 2026 — [Google — Atualizações da documentação da Pesquisa (changelog)](https://developers.google.com/search/updates)) e sem `Course`
(o Course Info saiu dos resultados em 2025: [Google — Simplificação da página de resultados (Course Info descontinuado, 2025)](https://developers.google.com/search/blog/2025/06/simplifying-search-results)). Sem promessa
de resultado enriquecido.

## Benefícios esperados

- Título e descrição alinhados à intenção principal → mais impressões
  relevantes e CTR (a confirmar no Search Console).
- Canonical absoluto → sinais concentrados no domínio de produção
  ([Google — Como especificar uma URL canônica](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls)).
- `WebSite` com `name` no subdomínio → chance de o Google exibir o nome do site
  em vez do host ([Google — Nomes de sites na Pesquisa (subdomínios)](https://developers.google.com/search/docs/appearance/site-names)).
- Preview correto no WhatsApp/redes (tráfego de compartilhamento).
