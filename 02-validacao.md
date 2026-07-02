# Playbook 02 — VALIDAÇÃO de oferta

> Objetivo: confirmar que a oferta minerada é real, lucrativa e **modelável** — e extrair a engenharia dela para reconstruir melhor.

## 1) Teardown do funil (use `WebFetch` na página de destino)

Disseque e anote:

- **Big idea / promessa central:** qual é a grande ideia única? (não o produto — a IDEIA)
- **Mecanismo único do problema** (por que o lead falhou até hoje) e **mecanismo único da solução** (o "como" novo).
- **Avatar:** quem é, dor primária, desejo, objeções, nível de consciência.
- **Estrutura da oferta:** produto principal, preço, ancoragem, **bônus**, **garantia**, escassez, parcelamento.
- **Tipo de página:** VSL, advertorial (matéria), quiz, página longa de texto, webinar.
- **Checkout:** Hotmart / Kiwify / Eduzz / Monetizze / Cartpanda / Ticto / Perfectpay…
- **Order bump / upsell** visíveis? Qual o AOV provável?

## 2) Níveis de consciência (Eugene Schwartz)

Identifique onde o lead está — isso define seu ângulo:

| Nível | Estado do lead | Ângulo que funciona |
|---|---|---|
| **Inconsciente** | Não sabe que tem o problema | História/curiosidade, "callout" do sintoma |
| **Consciente do problema** | Sente a dor, não conhece solução | Agitar dor + apresentar categoria de solução |
| **Consciente da solução** | Sabe que existe solução, não seu produto | Mecanismo único + prova |
| **Consciente do produto** | Conhece seu produto | Oferta + bônus + garantia + escassez |
| **Mais consciente** | Só falta o gatilho | Promoção/urgência direta |

## 3) Sofisticação de mercado

Quão batido está o nicho? Quanto mais maduro, mais você precisa de **mecanismo único** e **prova**, não só promessa maior.

- **Estágio 1–2:** promessa direta ainda funciona.
- **Estágio 3:** entra o **mecanismo único** ("o método X").
- **Estágio 4:** elabore o mecanismo (por que ESTE mecanismo é superior).
- **Estágio 5:** identificação/experiência/nova big idea (o mercado já ouviu tudo).

## 4) Validação de demanda

- `WebSearch` por volume de busca, fóruns, grupos, reclamações, concorrentes.
- Sinal verde: gente buscando solução, comunidades ativas, concorrentes vendendo há tempo.

## 5) Benchmarks de viabilidade (calibrar a conta)

Use `ads_insights_industry_benchmark` / `ads_insights_auction_ranking_benchmarks` para puxar números reais do nicho. Ranges típicos de referência no BR (validar sempre com a ferramenta):

| Métrica | Faixa de referência (infoproduto BR, frio) |
|---|---|
| CPM | R$ 10–40 |
| CTR (link) | 1%–3% |
| CPC (link) | R$ 0,50–2,50 |
| Conversão de VSL→checkout | 1%–5% |
| Conversão de checkout | 30%–60% |

> São referências de ordem de grandeza para sanidade — **sempre** prefira o número que a ferramenta de benchmark devolver.

## 6) Conta de viabilidade (go / no-go)

```
Receita por venda (ticket líquido + AOV de bump/upsell) = R$ ____
CPA-alvo máximo = Receita por venda ÷ ROAS break-even desejado
ROAS break-even = 1 ÷ margem  (ex.: margem 100% no digital → break-even ROAS ≈ 1; meta saudável ≥ 1,8–2,5)
```

Estime: CPC × (1 ÷ taxa de conversão do funil) = CPA estimado.
**Decisão:** se CPA estimado < CPA-alvo com folga → **GO**. Caso contrário, reveja oferta/ângulo ou descarte.

## Entregável desta fase

Salve em `outputs/<nicho>-<data>/02-validacao.md`:
- Teardown completo (big idea, mecanismos, avatar, oferta, funil).
- Nível de consciência + estágio de sofisticação → **ângulo recomendado**.
- Tabela de benchmarks + conta de viabilidade.
- Veredito **GO / NO-GO** com justificativa.
