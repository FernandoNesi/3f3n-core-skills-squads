# ============================================
# 3F3N SKILL
# ============================================

## NAME
ANALYSER_14_LOW_TICKET_3F3N

## VERSION
1.0

## LEVEL
Engine de Conversão (Nível 2)

## CATEGORY
Conversion / Audit / Low Ticket

---

## 🎯 PURPOSE

Identificar onde uma página de vendas low ticket está perdendo dinheiro,
quantificar o impacto e priorizar ações com base em conversão.

Essa skill NÃO cria páginas.
Ela mede e orienta decisão.

---

## 📥 INPUT

- URL ou conteúdo da página
- Público-alvo
- Ticket (R$)
- Tipo de tráfego (frio / morno / quente)

---

## ⚙️ EXECUTION FLOW

### ETAPA 1 — RAIO-X (5 segundos)

Responder:

1. Está claro o que está sendo vendido?
2. Existe desejo imediato?
3. Existe urgência?

Se qualquer resposta for NÃO:
→ marcar como FALHA CRÍTICA

---

### ETAPA 2 — FUNDAMENTOS

Pontuar (0–10):

- Clareza
- Interesse
- Confiança
- Ação

---

### ETAPA 3 — ANÁLISE 14 BLOCOS

Validar:

1. Promessa
2. Prova social
3. Dor
4. Transição
5. Passo a passo
6. Oferta + bônus
7. Para quem serve
8. Ancoragem
9. Preço + CTA
10. Conversa séria
11. Autoridade
12. CTA repetido
13. FAQ
14. Rodapé

Para cada bloco:

- Existe (sim/não)
- Qualidade (0–10)
- Impacto (baixo/médio/alto)

---

### ETAPA 4 — DETECÇÃO DE VAZAMENTOS

Identificar:

- Promessa fraca
- Falta de prova
- Falta de urgência
- Baixa percepção de valor
- Excesso de fricção
- Desalinhamento com público

---

### ETAPA 5 — IMPACTO FINANCEIRO

Classificar cada problema:

- 🔴 Alto impacto (+20%)
- 🟡 Médio impacto (10–20%)
- ⚪ Baixo impacto (<10%)

---

### ETAPA 6 — SCORE FINAL

Calcular:

0–100

Base:

- Fundamentos (40%)
- Estrutura (40%)
- Persuasão (20%)

---

## 📤 OUTPUT FORMAT (OBRIGATÓRIO)

Responder SEMPRE neste formato:

```markdown
# SCORE FINAL: X/100

# 💸 PERDA ESTIMADA
Conversão potencial: X%
Conversão atual estimada: X%
Perda: X% do faturamento

# 🔴 PRINCIPAIS VAZAMENTOS

1. [Problema] → impacto estimado
2. [Problema] → impacto estimado
3. [Problema] → impacto estimado

# ⚡ PRIORIDADE DE AÇÃO

1. [Ação]
2. [Ação]
3. [Ação]

# 🧠 FUNDAMENTOS

Clareza: X/10  
Interesse: X/10  
Confiança: X/10  
Ação: X/10
```