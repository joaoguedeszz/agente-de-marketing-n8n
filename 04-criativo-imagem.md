# Playbook 04 — CRIATIVO DE IMAGEM (e o PROMPT que converte)

> Objetivo: produzir a peça visual que **para o scroll** e puxa o clique. Duas vias:
> **(A)** gerar a imagem aqui (`generate_image`), ou **(B)** entregar um **prompt pronto** para o usuário rodar em outra IA. Esta é a via que o usuário pediu com ênfase — então o prompt tem que ser cirúrgico.

## O que faz uma imagem CONVERTER (não só ser bonita)

1. **Pattern interrupt:** destoa do feed. Rosto com emoção real, cor inesperada, enquadramento estranho-na-medida-certa.
2. **Parece nativo, não anúncio:** no frio, foto "de celular", print, screenshot, meme-style e UGC convertem mais que arte de estúdio polida. Anúncio com cara de anúncio é ignorado.
3. **Emoção no rosto:** olhar na câmera, expressão (alívio, choque, alegria, preocupação) que espelha o estado do avatar.
4. **Curiosidade visual:** algo que o cérebro precisa "resolver" → leva ao clique.
5. **Foco único:** um sujeito, um ponto focal. Nada poluído.
6. **Contraste para mobile:** 90% vê no celular, tela pequena, som off. Legível em 1 segundo.
7. **Prova ou antes/depois** (quando permitido e verdadeiro) — respeitando política (ver `06`).

## Formatos e proporções

| Posicionamento | Proporção | Uso |
|---|---|---|
| Feed | 1:1 ou 4:5 | 4:5 ocupa mais tela no mobile |
| Stories / Reels | 9:16 | tela cheia |
| Right column | 1:1 | secundário |

## Texto na imagem

- **Headline curta e grande** (3–7 palavras) que entrega o ângulo. O texto faz o trabalho pesado.
- Muitas IAs de imagem **erram texto**. Estratégias:
  1. Gere a imagem **com área limpa reservada** para o texto e adicione o texto depois (Canva/editor).
  2. Ou peça texto curtíssimo e cheque a renderização.
- Sempre **entregue separadamente** a copy do texto-overlay (headline + selo/CTA), mesmo quando o prompt pedir o texto embutido.

## A FÓRMULA DO PROMPT (preencha todos os blocos)

```
[ESTILO/MÍDIA] + [SUJEITO + EMOÇÃO] + [AÇÃO/POSE] + [CENÁRIO] +
[COMPOSIÇÃO/ENQUADRAMENTO] + [LUZ] + [CÂMERA/LENTE] + [PALETA/CLIMA] +
[ÁREA RESERVADA P/ TEXTO] + [PROPORÇÃO] + [NEGATIVE PROMPT]
```

Blocos:
- **Estilo/mídia:** "foto realista estilo celular/UGC", "fotografia editorial", "screenshot de app", "still cinematográfico".
- **Sujeito + emoção:** quem é o avatar + a emoção exata.
- **Ação/pose:** o que faz; olhar para a câmera costuma converter mais.
- **Cenário:** ambiente coerente com o avatar (cozinha real, quarto, rua, escritório caseiro).
- **Composição:** "close no rosto", "regra dos terços", "espaço negativo à esquerda para texto".
- **Luz:** "luz natural suave de janela", "golden hour", "luz dura realista".
- **Câmera/lente:** "35mm", "50mm f/1.8 fundo desfocado", "grande angular de celular".
- **Paleta/clima:** cores e emoção (quente/aconchegante, frio/clínico, vibrante).
- **Área para texto:** "deixe o terço superior limpo para headline".
- **Proporção:** 1:1 / 4:5 / 9:16.
- **Negative prompt:** "sem texto distorcido, sem mãos deformadas, sem marca d'água, sem logo, sem rosto plástico/artificial".

## Modelos de prompt prontos (adapte sujeito/nicho)

**1) UGC nativo (alta conversão no frio):**
> Foto realista estilo celular, mulher brasileira 45 anos, expressão de alívio e surpresa olhando direto para a câmera, segurando o celular em casa, cozinha real ao fundo levemente desfocada, luz natural de janela, lente de smartphone 26mm, cores quentes e aconchegantes, terço superior limpo para headline, proporção 4:5. Negative: texto distorcido, mãos deformadas, marca d'água, aparência de banco de imagens, pele plástica.

**2) Antes/depois (estado emocional — sem claim físico proibido):**
> Díptico fotográfico realista, à esquerda mulher cansada e desanimada em luz fria, à direita a mesma mulher confiante e sorrindo em luz quente, mesmo enquadramento de retrato, fundo neutro, 50mm f/2.0, contraste emocional claro, espaço inferior para legenda, proporção 1:1. Negative: texto, números de medida, claims, marca d'água, deformação.

**3) Curiosidade/pattern interrupt:**
> Still cinematográfico, homem 30 anos surpreso olhando para um caderno/notebook com algo fora de quadro, iluminação dramática lateral, cores contrastantes, composição com espaço negativo à direita para texto, 35mm, clima de "descoberta", proporção 4:5. Negative: texto distorcido, mãos extras, logo, watermark.

**4) Autoridade/mentor:**
> Retrato editorial de especialista confiante, braços cruzados, ambiente de escritório real, luz suave de softbox, 85mm fundo desfocado, paleta sóbria e profissional, espaço lateral para headline e selo, proporção 4:5. Negative: aparência artificial, texto, watermark, deformação.

## Para VÍDEO (quando aplicável)

- O **hook dos 3 primeiros segundos** decide tudo. Roteirize o hook visual + falado.
- Gere com `generate_video` e **valide o hook com `virality_predictor`** antes de subir.
- Estruture: hook (0–3s) → tensão/curiosidade (3–10s) → prova/mecanismo → CTA.

## Entregável

Para cada criativo, entregue: **prompt(s) de imagem completo(s)**, o **texto-overlay** (headline + selo/CTA), proporção, e — se gerado aqui — o **arquivo da imagem** salvo em `outputs/<nicho>-<data>/03-criativos/`.
