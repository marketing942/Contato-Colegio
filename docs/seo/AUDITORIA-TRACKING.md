# Auditoria de tracking — Contato Colégio CPPEM

Repositório: [`marketing942/Contato-Colegio`](https://github.com/marketing942/Contato-Colegio) · branch `seo/otimizacao-organica-20261023` (base `main`) · 23/10/2026
Relatório consolidado do ecossistema: [RELATORIO-GERAL-SEO-ECOSSISTEMA.md](RELATORIO-GERAL-SEO-ECOSSISTEMA.md)

Regra seguida: nenhum ID, evento, parâmetro, script, seletor, endpoint, UTM ou
regra de consentimento foi alterado. Nenhum token ou credencial aparece aqui.

## Inventário

| Integração | Onde | Detalhe |
|---|---|---|
| GTM server-side (loader first-party) | `index.html`, 1º script do `<head>` | `https://sgtm.cppem.com.br/metrics/` — o ID do container está no path; mesmo container das demais landings |
| GTM noscript | `index.html`, `<body>` | `https://sgtm.cppem.com.br/ns.html?id=GTM-PJ379FLQ` |
| PixelX | carregada pelo GTM (`pxa.cppem.com.br`) | máscara de telefone `.pxa_mask_phone`; o Lead é a regra do painel vinculada ao `id` do `<form>` |
| Formulário | `form#eiBtTROiAlNexbHXklSc` (name `lead_form`) | campos lead_name/lead_email/lead_phone |
| Planilha de leads | POST Apps Script `?aba=COLEGIO` | email, nome, origem, pagina_url, telefone, utm_campaign, utm_source |
| Redirecionamento | `script.js` linha ~207 | `wa.me/5581997076388` |
| Vídeo | script inline | YouTube nocookie só após clique |

## Antes × depois

- Arquivos de tracking/fluxo (`script.js`, `styles.css`, `google-apps-script.js`, `validar-tracking.js`, `vercel.json`): **sem nenhuma alteração** (`git diff` vazio).
- Mudanças só em `<head>` (metadados/JSON-LD), arquivos novos (robots, sitemap,
  imagens OG) e imagens otimizadas com o mesmo nome.
- Resultado dos testes de execução: ver [RELATORIO-DE-TESTES.md](RELATORIO-DE-TESTES.md).

## Classificação

- GTM loader, noscript, dataLayer, formulários, campos enviados à planilha,
  UTMs e redirecionamentos: **validado por teste de execução** (antes × depois idênticos).
- Lead da PixelX / conversões no Meta e no GTM server-side: **não validado por falta de acesso**.

## Riscos remanescentes

- Nenhum risco novo.
