# Playbook 05 — FUNIL de vendas validado (infoproduto)

> Objetivo: montar o caminho completo do clique à venda (e ao LTV), escolhendo o arquétipo certo e **fechando a matemática**.

## Escolha do arquétipo (pela consciência do lead × ticket)

| Arquétipo | Quando usar | Fluxo |
|---|---|---|
| **VSL direta** | Lead consciente do problema/solução, low/mid-ticket | Anúncio → VSL → checkout → bump → upsell |
| **Advertorial → VSL** | Lead mais frio, mercado batido | Anúncio → advertorial (matéria) → VSL → checkout |
| **Quiz funnel** | Segmentar + aquecer + capturar lead | Anúncio → quiz → resultado/VSL → oferta |
| **Webinar perpétuo** | Mid/high-ticket, precisa educar | Anúncio → inscrição → webinar → oferta + carrinho |
| **Lançamento (PLF)** | High-ticket, evento | Captação → CPL 1/2/3 → carrinho aberto/fechado |
| **Low-ticket → upsell** | Escala fria + monetização no AOV | Anúncio → oferta R$9–47 → upsells → high-ticket no back-end |

Justifique a escolha pelo diagnóstico da Fase 2 (consciência/sofisticação) e pelo ticket.

## Diagrama-base (VSL com monetização)

```
 ANÚNCIO (Meta)
     │  (CTR, CPC)
     ▼
 PÁGINA (advertorial/VSL/quiz)
     │  (retenção da VSL, % chega na oferta)
     ▼
 CHECKOUT  ──►  ORDER BUMP (+R$)  (take-rate 20–40%)
     │
     ▼
 UPSELL 1 (one-click)  ──► (não) ──►  DOWNSELL
     │ (sim)                              │
     ▼                                    ▼
 UPSELL 2 / high-ticket            PÁGINA DE OBRIGADO
     │
     ▼
 SEQUÊNCIA E-MAIL + WHATSAPP  +  REMARKETING (não compradores)
```

## Construção da OFERTA (equação de valor — Hormozi)

```
Valor percebido = (Sonho realizado × Probabilidade percebida de sucesso)
                  ─────────────────────────────────────────────────────
                  (Tempo até o resultado × Esforço/sacrifício)
```

Maximize numerador, minimize denominador:
- **Sonho:** resultado específico e desejado.
- **Probabilidade:** prova, garantia, mecanismo crível, depoimentos.
- **Tempo:** "primeiros resultados em X dias".
- **Esforço:** "sem precisar de ___", passo a passo, feito-para-você.

**Stack de valor:** produto principal + bônus que destroem objeções + ancoragem ("valor total R$X, hoje R$Y") + **garantia** (incondicional 7–30 dias) + **escassez legítima** (turma, bônus por tempo limitado — nunca falsa).

## Monetização (subir o AOV)

- **Order bump:** complemento barato e óbvio no checkout (take-rate 20–40%).
- **Upsell 1 (one-click):** versão premium/aceleração logo após a compra.
- **Downsell:** versão menor para quem recusou o upsell.
- **Back-end:** high-ticket (mentoria/comunidade) por e-mail/WhatsApp/remarketing — é onde mora o lucro real.

## Follow-up (recuperação e LTV)

- **E-mail:** boas-vindas → entrega de valor → quebra de objeção → prova → oferta/urgência (5–7 e-mails).
- **WhatsApp:** recuperação de checkout abandonado, lembrete de bônus, oferta do back-end.
- **Remarketing Meta:** públicos de quem viu a VSL/iniciou checkout e não comprou (ângulo de objeção + urgência).

## Rastreamento (sem isso, não há validação)

- **Pixel + Conversions API (CAPI)** com eventos: ViewContent, InitiateCheckout, Purchase, e custom (lead, % de VSL).
- **UTMs** em todos os links para atribuir por criativo/ângulo.
- Confira a correspondência de eventos (event match quality) para o algoritmo otimizar.

## A MATEMÁTICA DE VALIDAÇÃO (o funil só é "validado" aqui)

```
Receita por comprador (AOV) = ticket + (bump × take) + (upsells × take) ...
ROAS break-even             = 1 ÷ margem  (digital ≈ 1, então break-even ROAS ≈ 1; meta ≥ 1,8–2,5)
CPA-alvo                    = AOV ÷ ROAS-meta
EPC (ganho por clique)      = Receita total ÷ cliques
```

**Regra de validação:** o funil está validado quando, em volume estatístico (≥ ~50–100 conversões ou orçamento de teste suficiente), o **CPA real < CPA-alvo** e o **ROAS > break-even** de forma consistente.

## Regras de escala e corte

- **Corte de criativo:** sem venda após gastar ~1–2× o CPA-alvo → mata.
- **Escala vencedor:** duplicar/aumentar budget 20–50% a cada 2–3 dias mantendo CPA; ou abrir CBO com os vencedores.
- **Teste contínuo:** sempre 70% no que funciona, 30% testando ângulo/criativo novo.
- Diagnostique por etapa: CTR baixo → criativo/hook; clica e não compra → página/oferta; compra e não fica → entrega/produto.

## Entregável

Use `templates/funil.md`. Salve em `outputs/<nicho>-<data>/04-funil.md`:
- Arquétipo escolhido + diagrama.
- Oferta montada (stack, preço, bônus, garantia).
- Copy/estrutura de cada etapa (página, bump, upsells, e-mails, WhatsApp).
- Plano de rastreamento + **planilha de números** (AOV, CPA-alvo, ROAS-meta, KPIs por etapa).
- Plano de teste, escala e corte.
