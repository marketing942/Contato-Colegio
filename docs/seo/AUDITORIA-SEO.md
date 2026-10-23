# Auditoria SEO — Contato Colégio CPPEM

Repositório: [`marketing942/Contato-Colegio`](https://github.com/marketing942/Contato-Colegio) · branch `seo/otimizacao-organica-20261023` (base `main`) · 23/10/2026
Relatório consolidado do ecossistema: [RELATORIO-GERAL-SEO-ECOSSISTEMA.md](RELATORIO-GERAL-SEO-ECOSSISTEMA.md)

## Arquitetura

- **Domínio de produção:** não identificado com certeza (padrão `colegio*.cppem.com.br`) — evidência: o Apps Script reconhece `//colegio[a-z0-9.-]*\.cppem\.com\.br` — o host exato não aparece no código.
- **Stack:** HTML + CSS (inline) + JavaScript estáticos. Vercel. Fontes do Google (Nunito, Nunito Sans). Vídeo YouTube (nocookie) sob clique.
- **Renderização:** HTML estático com todo o conteúdo no HTML inicial.

## Rotas

| Rota | O que é | Indexação |
|---|---|---|
| / | Contato/matrículas do Colégio CPPEM (formulário → planilha → WhatsApp) | Indexar |

## Finalidade e classificação

- **Objetivo:** Captar famílias interessadas em matrícula (Matrículas 2027). CTA: "QUERO ENTRAR EM CONTATO".
- **Unidade de negócio:** Colégio CPPEM
- **Público:** Pais e responsáveis em Caruaru-PE (1º ano do Fundamental ao 3º ano do Médio).
- **Tipo de página:** Página de captura com conteúdo institucional (pilares, depoimentos, nova sede, endereços).
- **Indexação recomendada:** Indexar. É a página do Colégio neste escopo com mais informação local verificável (endereços, telefones, portaria de credenciamento).
- **Potencial orgânico:** **Alto (local)** — Busca local por escola particular tem intenção forte e sazonalidade agora (matrículas 2027). Concorrentes locais aparecem em agregadores (Melhor Escola, Escol.as, Quero Bolsa).

## Problemas encontrados

Gravidade: **P0** crítico (indexação/integridade) · **P1** alto impacto · **P2** médio · **P3** evolução · **Info** registro sem ação de SEO.

| Sev. | Problema | Evidência | Impacto | Status |
|---|---|---|---|---|
| P1 | Title sem termo de busca | `Colégio CPPEM — Fale com a gente` | Não aparece para "escola cristã/militarizada em Caruaru" | Corrigido |
| P1 | Domínio final desconhecido | Sem canonical, `og:url`, `og:image` | Duplicação com `*.vercel.app`; preview sem imagem | Pendente (informar o domínio) |
| P1 | Sem dados estruturados de escola |  | Google sem endereço/telefone da entidade nesta página | Corrigido (School) |
| P2 | Imagens maiores que o exibido | Lighthouse: ~1,9 MB de economia possível em celular (pilares, depoimentos PNG, fotos) | Peso/LCP | Recomendado (precisa medir o tamanho exibido de cada uma) |
| P2 | Dois endereços | Rodapé: Praça Presidente Getúlio Vargas, 119 (atual) e Rodovia PE-095, 562 (nova sede) | NAP inconsistente quando houver a mudança | Documentado (JSON-LD usa o atual) |
| P2 | Google Business Profile | Fora do código | É o principal fator do pacote local (mapa) | Recomendado |
| P3 | Possível canibalização com o site institucional do Colégio | Outro repositório fora do escopo |  | Recomendado (definir URL dona de "Colégio CPPEM") |

## Limitações desta auditoria

- **Produção inacessível desta sessão.** O proxy de rede do ambiente recusou
  conexões a `*.cppem.com.br` e `*.vercel.app`, e o leitor de páginas não
  resolveu esses domínios. Nada foi medido no site publicado: HTML servido,
  status HTTP, redirecionamentos e headers reais ficam **não validados**.
  Toda a auditoria foi feita no código e em servidores locais.
- **Sem Google Search Console, GA4, Keyword Planner, Trends, Semrush ou Ahrefs.**
  Não há volume, dificuldade, CPC nem posição. Nenhum número desse tipo
  aparece aqui. As prioridades de palavra-chave são **estimativas
  qualitativas** (intenção, tipo de página que aparece hoje, relevância
  comercial) e devem ser confirmadas no Search Console e no Planejador.
- **SERP observada com a busca web disponível, que não é o Google.** Os
  concorrentes listados são os que apareceram nessa busca e servem como
  indício, não como ranking do Google.
- **Lighthouse é dado de laboratório**, rodado localmente com os terceiros
  (GTM, PixelX, fontes do Google) bloqueados. Serve para comparar antes ×
  depois, não para prever o Core Web Vitals real (dado de campo do CrUX).
