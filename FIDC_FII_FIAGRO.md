# Guia Prático de Gestão — FIDC · FII · FIAGRO

**Gestão Ativa · Valuation · Asset Allocation · Trading · Estruturação · Controle de Risco**

*Com Fontes e Referências de Mercado — Edição 2025*

> Para: Gestores de Recursos | Especialistas de Produto | Analistas Sênior

---

# Nota sobre as Fontes e Referências

Este guia integra ao longo de cada seção as fontes primárias e secundárias utilizadas como base das análises e recomendações. As fontes seguem a convenção [Fonte: ...] imediatamente após o conteúdo ao qual se referem e são categorizadas em:

- Regulatórias: normas da CVM, Banco Central, legislação federal e portarias ministeriais

- Institucionais: publicações da ANBIMA, B3, IBGE, MAPA, INPE, IBAMA e outras autarquias

- Mercado: relatórios de consultorias (CBRE, JLL, SiiLA, Buildings), agências de rating (Fitch, Moody's Local, S&P), provedores de dados (Quantum, Economatica)

- Acadêmicas e Técnicas: artigos, manuais operacionais e publicações setoriais

As fontes são indicadas para orientar o leitor à leitura primária. Dado o caráter dinâmico das normas e dos dados de mercado, recomenda-se sempre verificar a versão mais recente de cada documento.

---

# PARTE I
## FUNDOS DE INVESTIMENTO IMOBILIÁRIO — FII
*Gestão Ativa, Valuation e Rotinas Operacionais*
# 1. Mapeamento e Análise do Universo de FIIs
O ponto de partida da gestão ativa de FIIs é a construção de um universo de cobertura estruturado. O mercado brasileiro conta com mais de 400 FIIs listados na B3, com valor de mercado agregado superior a R$ 400 bilhões e mais de 2,5 milhões de investidores pessoas físicas cadastrados.

> 📎 **Fonte:** B3 — Boletim Mensal de Fundos Imobiliários, março 2025; CVM — Painel de Fundos de Investimento, 2025

## 1.1 Segmentação do Universo
| **Segmento**        | **Subclasse**                   | **Drivers de Valor**                      | **Benchmark de Renda** |
|---------------------|---------------------------------|-------------------------------------------|------------------------|
| Lajes Corporativas  | AAA, AA, Trophy, Suburbano      | Vacância, absorção líquida, CAGR ABL      | NTN-B + spread         |
| Logística / Galpões | BTS, cross-dock, last-mile      | E-commerce, nearshoring, locatário âncora | IGP-M ou IPCA + spread |
| Shopping Centers    | Premium, Regional, Conveniência | SSS, SAS, NOI/m², vacância financeira     | CDI ou IPCA + spread   |
| Renda Urbana        | Varejo de rua, agências         | Qualidade do locatário, contrato atípico  | IPCA + spread fixo     |
| Saúde e Educação    | Hospitais, clínicas, faculdades | Contratos atípicos 15–20 anos             | CDI+ ou IPCA+          |
| CRI AAA/AA          | IPCA+, CDI+, prefixado          | Duration, spread, LTV, rating garantidor  | NTN-B ou CDI           |
| CRI Mid-High Yield  | Devedores mid-cap               | Spread x risco, covenants, concentração   | CDI + spread alto      |
| FoF / Híbrido       | Carteiras diversificadas        | Desconto P/VP, gestão, governança         | IFIX                   |

> 📎 **Fonte:** ANBIMA — Classificação de Fundos de Investimento (2024); B3 — Regulamento de Segmentos de Listagem

## 1.2 Triagem Quantitativa — Filtros de Entrada
- Liquidez mínima: ADV ≥ R$ 500 mil nos últimos 90 dias — critério eliminatório para fundos institucionais

- PL mínimo: R$ 300 milhões — garante estrutura operacional e menor risco de descontinuidade

- Histórico mínimo: 24 meses de dados operacionais e de distribuição

- Número de cotistas: \>1.000 cotistas PF registrados na CVM

> 📎 **Fonte:** ANBIMA — Código ART (Administração de Recursos de Terceiros), 2023; CVM — Instrução Normativa sobre Elegibilidade de FIs

## 1.3 Fontes de Dados e Ferramentas
| **Fonte**                  | **Dados Disponíveis**                                 | **Frequência**                 | **Acesso**                                 |
|----------------------------|-------------------------------------------------------|--------------------------------|--------------------------------------------|
| CVM — DRI / Dados Abertos  | Informes mensais, demonstrações, relatórios de gestão | Mensal / Anual                 | Gratuito; API em dados.cvm.gov.br          |
| B3 — Portal de Dados       | Preços, volumes, lotes, ex-dividendos, IFIX           | Diário (EOD gratuito; RT pago) | Gratuito (EOD) / Pago (RT)                 |
| ANBIMA — Portal de Dados   | Valor patrimonial, emissões, benchmarks de fundos     | Diário / Mensal                | Gratuito para associados                   |
| Quantum Axis / Economatica | Séries históricas consolidadas, screener, backtesting | Diário                         | Pago — padrão de mercado BR                |
| SiiLA Brasil / Buildings   | Vacância, absorção, ABL, cap rates setoriais          | Trimestral / Mensal            | Pago — especializado imobiliário           |
| CBRE / JLL Relatórios      | Ciclo imobiliário, relatórios setoriais de mercado    | Trimestral                     | Gratuito (versão pública)                  |
| Relatórios Gerenciais FIIs | NOI, vacância, inadimplência, agenda de vencimentos   | Mensal                         | Gratuito — sites das gestoras              |
| IBGE — SIDRA               | Inflação (IPCA/IGP), construção civil, PIB setorial   | Mensal / Trimestral            | Gratuito — sidra.ibge.gov.br               |
| FGV — IBRE                 | IGP-M, IPC-A, custo da construção (CUB/SINAPI)        | Mensal                         | Gratuito (síntese) / Pago (série completa) |

> 📎 **Fonte:** CVM — Portal Dados Abertos (dados.cvm.gov.br); ANBIMA — Portal de Informações e Estatísticas (anbima.com.br)

# 2. Teses de Investimento e Asset Allocation em FIIs
## 2.1 Asset Allocation Macro: Tijolo vs. Papel
| **Cenário Macro**                    | **Posicionamento Tijolo**      | **Posicionamento Papel** | **Racional**                                                   |
|--------------------------------------|--------------------------------|--------------------------|----------------------------------------------------------------|
| Juros altos + inflação elevada       | Underweight (30–40%)           | Overweight (60–70%)      | Custo de capital alto penaliza imóveis; CRI IPCA+ retornam bem |
| Juros em queda + inflação controlada | Overweight (60–70%)            | Underweight (30–40%)     | Cap rate compression eleva P/VP; tijolo aprecia                |
| Juros neutros + macro incerto        | Neutro (50/50)                 | Neutro (50/50)           | Diversificação defensiva; preferência por qualidade            |
| Recessão + vacância alta             | Underweight; foco em qualidade | Neutro; evitar mid-yield | Contratos atípicos; evitar devedor frágil                      |
| Ciclo imobiliário expansivo          | Overweight (65–75%)            | Reduzido                 | Absorção de espaços; pressão altista de aluguel                |

> 📎 **Fonte:** JLL Research Brasil — Relatório de Mercado Imobiliário Corporativo Q4/2024; CBRE Research — Cap Rate Survey Brasil 2024

## 2.2 Framework de Seleção de FIIs
### 2.2.1 Análise Quantitativa (50% do score)
| **Métrica**                   | **Peso** | **Como Calcular**                                      | **Referência Saudável**                                     |
|-------------------------------|----------|--------------------------------------------------------|-------------------------------------------------------------|
| Dividend Yield (DY) 12M       | 15%      | Soma distribuições 12M / Preço atual                   | CDI líquido PF + 2–4 pp (estimado em 12–15% em 2025)        |
| P/VP                          | 15%      | Preço mercado / Valor patrimonial (último informe CVM) | 0,85–1,05x (\< 0,85 = oportunidade ou risco; \>1,10 = caro) |
| Cap Rate dos ativos (tijolo)  | 10%      | NOI anual / Valor justo dos imóveis (laudo)            | NTN-B 10A + 200–300 bps                                     |
| Vacância financeira           | 5%       | Receita não realizada / Receita potencial total        | \< 10% (tijolo prime); \< 5% (contratos atípicos)           |
| Consistência de distribuições | 5%       | CV = Desvio padrão / Média das distribuições           | CV \< 15% = consistente; \> 30% = irregular                 |

> 📎 **Fonte:** ANBIMA — Manual de Marcação a Mercado (2024); CVM — Instrução sobre Informes de FIIs

### 2.2.2 Análise Qualitativa (50% do score)
| **Critério**             | **Peso** | **O que Avaliar**                                                                                |
|--------------------------|----------|--------------------------------------------------------------------------------------------------|
| Qualidade da gestora     | 20%      | Track record auditado, equipe, turnover, alinhamento de interesses, transparência dos relatórios |
| Qualidade dos ativos     | 15%      | Localização (A/B/C), especificação técnica, certificações (LEED, AQUA), estado de conservação    |
| Qualidade dos locatários | 10%      | Rating, diversificação, setor, histórico de pagamento, prazo remanescente dos contratos          |
| Governança e conflitos   | 5%       | Partes relacionadas, taxa de performance, política de desinvestimento, transparência em AGEs     |

> 📎 **Fonte:** ANBIMA — Código ART 2023, Seções 3 e 4 (Dever Fiduciário e Gestão de Conflitos)

# 3. Valuation de FIIs
## 3.1 Cap Rate e NOI — FII de Tijolo
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>📐 Fórmula do Cap Rate</strong></td>
</tr>
<tr class="even">
<td><p>Cap Rate = NOI Anual / Valor Justo do Imóvel</p>
<p>NOI = Receita Bruta de Locação – Vacância – Despesas Operacionais do Imóvel (IPTU, condomínio vago)</p>
<p>Exemplo: NOI R$ 12M/ano e laudo R$ 150M → Cap Rate = 8,0% a.a.</p>
<p>Spread sobre NTN-B 10A (6,2% em jan/2025): 180 bps → avaliar se atrativo vs. risco de locação</p></td>
</tr>
</tbody>
</table>

> 📎 **Fonte:** CBRE Research — Brazil Cap Rate Report 2024; FGV-IBRE — Taxas de Desconto para Ativos Imobiliários

| **Segmento**                     | **Cap Rate Médio (2024–25)** | **Spread sobre NTN-B 10A** | **Avaliação**                                |
|----------------------------------|------------------------------|----------------------------|----------------------------------------------|
| Lajes AAA (SP/RJ)                | 7,5%–9,0%                    | 150–300 bps                | Prêmio razoável; sensível a juros            |
| Galpões AAA (BTS/mono)           | 7,0%–8,5%                    | 100–250 bps                | Comprimido; demanda forte; risco no contrato |
| Galpões multi-inquilino          | 8,5%–10,5%                   | 250–450 bps                | Spread adequado; maior risco operacional     |
| Shopping Premium                 | 8,0%–9,5%                    | 200–350 bps                | Ciclo de recuperação pós-pandemia            |
| Contratos Atípicos (saúde/educ.) | 10,0%–12,0%                  | 400–600 bps                | Prêmio de iliquidez; contrato muito longo    |

> 📎 **Fonte:** CBRE Research 2024; JLL Brasil Q4/2024; SiiLA Market Report 2025

## 3.2 NAV e P/VP
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>📐 Cálculo do NAV e P/VP</strong></td>
</tr>
<tr class="even">
<td><p>NAV = Σ(Valor Avaliação Imóveis) + Caixa + Outros Ativos – Dívidas</p>
<p>P/VP = Preço Mercado / (NAV / Nº de Cotas)</p>
<p>P/VP &lt; 1: desconto → potencial oportunidade (verificar se é risco ou ineficiência)</p>
<p>P/VP &gt; 1: prêmio → mercado precifica crescimento ou qualidade superior</p>
<p>Atenção: laudo semestral pode estar defasado → ajuste pelo Cap Rate corrente de mercado</p></td>
</tr>
</tbody>
</table>

> 📎 **Fonte:** CVM — Resolução 175/2022, Anexo III, art. 38 (obrigatoriedade do laudo semestral); ABNT NBR 14653 (avaliação de bens imóveis)

## 3.3 Valuation de FII de Papel — SAR
| **Dimensão**             | **Métricas**                             | **Sinal de Alerta**                                          |
|--------------------------|------------------------------------------|--------------------------------------------------------------|
| Duration / WAL           | Prazo médio ponderado em anos            | WAL \< 2 anos = reinvestment risk; \> 8 anos = duration risk |
| LTV médio                | Saldo devedor / Valor do ativo-garantia  | LTV \> 70% sem garantia adicional = risco de recuperação     |
| Spread médio             | Taxa dos CRIs – benchmark (CDI ou NTN-B) | Spread \> 5% sem explicação = risco de crédito embutido      |
| Concentração por devedor | % do PL no maior devedor                 | Devedor único \> 20% = concentração excessiva                |
| Rating da carteira       | % em AA ou superior                      | \< 50% em AA+ = carteira de crédito arriscado                |
| Tipo de devedor          | PF, PJ mid/large cap, loteamento         | Alta PF ou loteamento = risco difuso e difícil monitoramento |

> 📎 **Fonte:** ANBIMA — Informe de CRIs e CRAs 2024; Fitch Ratings — Metodologia de Rating de CRIs Brasil

# 4. Trading e Gestão do Fluxo de Caixa
## 4.1 Dinâmica do Mercado Secundário
- Lote padrão: 1 cota (fracionário e inteiro simultâneos); verificar antes de montar algoritmo

- Horário: 10h–18h20 (pregão B3); volumes concentrados nos primeiros e últimos 30 min

- Ex-dividendo: preço cai mecanicamente pelo valor da distribuição no ex-date

- Impacto de mercado: limite prático de ~5% do ADV numa única ordem

> 📎 **Fonte:** B3 — Manual de Negociação de Renda Variável; Manual de Operações do Mercado B3 (2024)

## 4.2 Estratégias de Execução
| **Estratégia**            | **Quando Usar**                             | **Como Implementar**                                | **Cuidado**                               |
|---------------------------|---------------------------------------------|-----------------------------------------------------|-------------------------------------------|
| TWAP                      | Posições grandes em fundos com ADV médio    | Dividir volume em fatias iguais ao longo do pregão  | Sinaliza intenção ao longo do dia         |
| VWAP                      | Fundos com distribuição de volume irregular | Executar proporcional ao perfil histórico de volume | Pode concentrar no final do pregão        |
| Ordens limite escalonadas | Reforço gradual de posição existente        | Lances em P, P-0,5%, P-1%                           | Não garante execução total no prazo       |
| Participação em follow-on | Fundo com tese e emissão atrativa           | Subscrever no período de reserva com desconto       | Avaliar diluição e uso dos recursos antes |

> 📎 **Fonte:** CVM — Resolução 160/2022 (ofertas públicas); B3 — Regulamento de Operações (2024)

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>🗓️ Rotina Semanal do Gestor — FoF de FIIs</strong></td>
</tr>
<tr class="even">
<td><p>Segunda: book de posições; atualização P/VP; ex-dividendos da semana</p>
<p>Terça: leitura dos relatórios gerenciais publicados; atualização de modelos de valuation</p>
<p>Quarta: comitê de gestão; decisões de compra/venda; análise de follow-ons abertos</p>
<p>Quinta: execução de ordens aprovadas; acompanhamento de liquidez</p>
<p>Sexta: fechamento; cálculo do PL e cota; relatório semanal interno</p>
<p>Diário: monitoramento de preços; eventos (CMR, AGE, informes extraord.)</p></td>
</tr>
</tbody>
</table>

> 📎 **Fonte:** ANBIMA — Código ART 2023, Seção 6 (Processo de Gestão e Rotinas Operacionais)

# 5. Relatórios e Relacionamento com Investidores
## 5.1 Estrutura do Relatório Mensal de Gestão
| **Seção**                   | **Conteúdo Essencial**                                     | **Extensão**       |
|-----------------------------|------------------------------------------------------------|--------------------|
| 1\. Resumo Executivo        | DY do mês, performance vs IFIX, principais movimentos      | 1 página           |
| 2\. Contexto Macroeconômico | Curva de juros, inflação, visão do gestor                  | 1–2 páginas        |
| 3\. Performance da Carteira | Retorno total; atribuição por segmento                     | 1–2 páginas        |
| 4\. Análise dos Ativos      | Top 5–10 posições: tese, movimentos, atualiz. operacionais | 2–3 páginas        |
| 5\. Movimentações           | Compras, vendas, follow-ons; racional de cada decisão      | 1 página           |
| 6\. Outlook                 | Visão prospectiva; posicionamento para o cenário esperado  | 1–2 páginas        |
| 7\. Dados do Fundo          | PL, cota, DY, P/VP médio, distribuição por segmento        | 1 página (tabelas) |

> 📎 **Fonte:** CVM — Resolução 30/2021 (relatórios de gestão de FIIs); ANBIMA — Código ART 2023, Anexo I

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>⚠️ Erros Comuns na Comunicação com Investidores</strong></td>
</tr>
<tr class="even">
<td><p>• Relatório descritivo sem visão: descrever o que aconteceu sem opinar ou contextualizar</p>
<p>• Linguagem protocolada sem convicção: poderia ter sido escrito por qualquer gestor</p>
<p>• Omissão de fundos com performance negativa: survivorship bias no relatório</p>
<p>• DY nominal sem contextualizar o P/VP de entrada do investidor</p>
<p>• Mudança de tese sem explicação do racional ao cotista</p></td>
</tr>
</tbody>
</table>

> 📎 **Fonte:** ANBIMA — Guia de Melhores Práticas de Comunicação com Cotistas (2023)

---

# MÓDULO DE RISCO — FII
## Controle e Gestão de Risco para Fundos Imobiliários
*Frameworks, Dashboards, Limites e Processos Operacionais*
# 6. Controle e Gestão de Risco — FII
A gestão de risco de um FII — especialmente FoF ou FII de tijolo com PL relevante — envolve dimensões simultâneas: risco de mercado (variação de preços das cotas), risco de crédito (inadimplência de locatários e de devedores de CRI), risco de liquidez (capacidade de converter posições em caixa), risco operacional (falhas de processo) e risco regulatório. Um framework integrado é a única forma de manter visibilidade completa.

> 📎 **Fonte:** CVM — Resolução CVM 175/2022, Art. 62 a 67 (Gestão de Risco); ANBIMA — Código ART 2023, Seção 5

## 6.1 Taxonomia de Riscos do FII
| **Categoria**         | **Subcategoria**                     | **Fonte do Risco**                                        | **Instrumento de Medição**                                  |
|-----------------------|--------------------------------------|-----------------------------------------------------------|-------------------------------------------------------------|
| Risco de Mercado      | Variação de preço das cotas          | Taxa de juros (NTN-B, DI futuro); sentimento de mercado   | Duration; DV01; tracking error vs. IFIX                     |
| Risco de Mercado      | Variação de P/VP                     | Cap rate de mercado; laudo defasado                       | Monitoramento semanal P/VP vs. pares                        |
| Risco de Crédito      | Inadimplência de locatário (tijolo)  | Deterioração financeira do locatário; vacância após saída | Índice de cobertura de aluguel (EBITDA / Aluguel)           |
| Risco de Crédito      | Inadimplência de devedor CRI (papel) | Default do emissor do CRI; deterioração do lastro         | LTV atualizado; rating; índice de inadimplência da carteira |
| Risco de Liquidez     | Liquidez das cotas (secundário)      | ADV baixo; concentração de cotistas                       | ADV 90 dias; dias para liquidar posição                     |
| Risco de Liquidez     | Liquidez dos ativos (tijolo)         | Mercado imobiliário deprimido; imóvel mono-inquilino      | Prazo estimado de venda; cap rate de saída                  |
| Risco de Concentração | Ativo único / locatário único        | Alta dependência de um ativo ou inquilino                 | % do PL em único ativo; % da receita de único locatário     |
| Risco Operacional     | Falha nos processos do gestor        | Erro humano, falha de sistema, fraude interna             | Controles SOC; auditorias; checklists                       |
| Risco Regulatório     | Mudança de norma / tributação        | Alteração na legislação de isenção fiscal (Lei 8.668/93)  | Monitoramento legislativo; buffer de margem                 |

> 📎 **Fonte:** Fitch Ratings — Metodologia de Análise de FIIs (2024); ANBIMA — Código ART, Seção 5 (Controle de Risco)

## 6.2 Sistema de Limites — FII
Todo fundo deve ter uma Política de Gestão de Risco aprovada pelo administrador e pelo gestor, que estabelece limites quantitativos e qualitativos para cada dimensão de risco. Os limites abaixo são referência de mercado e devem ser calibrados conforme o mandato de cada fundo:

| **Limite**                        | **Métrica**         | **Alerta Amarelo** | **Alerta Vermelho** | **Ação Requerida**                               |
|-----------------------------------|---------------------|--------------------|---------------------|--------------------------------------------------|
| Concentração por ativo            | % do PL             | ≥ 15%              | ≥ 20%               | Reduzir posição; obter aprovação do comitê       |
| Concentração por segmento         | % do PL             | ≥ 30%              | ≥ 40%               | Revisão estratégica de alocação                  |
| Concentração por gestora (FoF)    | % do PL             | ≥ 25%              | ≥ 35%               | Diversificar entre gestoras                      |
| P/VP médio ponderado da carteira  | Múltiplo            | \> 1,15x           | \> 1,25x            | Reduzir posições mais caras; aumentar caixa      |
| Vacância média ponderada (tijolo) | % da área alugável  | ≥ 12%              | ≥ 18%               | Revisão dos contratos; plano de ocupação         |
| LTV médio da carteira de CRIs     | % do ativo-garantia | ≥ 65%              | ≥ 75%               | Revisão dos CRIs de maior LTV; redução gradual   |
| ADV mínimo das posições           | R$ / dia (90d)     | \< R$ 600k        | \< R$ 300k         | Plano de saída gradual; não aumentar posição     |
| Caixa mínimo                      | % do PL             | \< 3%              | \< 1,5%             | Não executar compras; monetizar posições menores |
| Duration da carteira de CRIs      | Anos                | \> 6 anos          | \> 8 anos           | Reduzir CRIs de prazo longo; aumentar CDI+       |

> 📎 **Fonte:** ANBIMA — Código ART 2023; CVM — Resolução 175/2022 Art. 64 (limites de concentração)

## 6.3 Dashboard de Risco — FII
O dashboard de risco é o painel central de monitoramento diário e semanal. Cada indicador deve ter um semáforo de status (verde / amarelo / vermelho) e um responsável pela ação corretiva:

| **Indicador**                        | **Frequência** | **Fonte dos Dados**                       | **Status (Exemplo)**     | **Responsável**     |
|--------------------------------------|----------------|-------------------------------------------|--------------------------|---------------------|
| P/VP médio ponderado                 | Diário         | B3 (preços) + CVM (VP do último informe)  | 🟡 1,08x (limite: 1,10x) | Gestor              |
| ADV 90 dias (posição mais ilíquida)  | Semanal        | B3 / Quantum                              | 🟢 R$ 2,1M              | Middle Office       |
| Dias para liquidar posições (75% PL) | Semanal        | Cálculo interno: posição / ADV 90d        | 🟢 8 dias úteis          | Middle Office       |
| Vacância financeira média (tijolo)   | Mensal         | Relatórios gerenciais dos FIIs investidos | 🟢 6,3%                  | Gestor              |
| Inadimplência de aluguéis            | Mensal         | Relatórios gerenciais dos FIIs investidos | 🟢 0,8%                  | Gestor              |
| LTV médio carteira de CRIs           | Mensal         | Informes dos FIIs de papel + relatórios   | 🟡 61% (limite: 65%)     | Analista de Crédito |
| Concentração máx. por ativo          | Semanal        | Sistema de gestão de carteira             | 🟢 9,2%                  | Middle Office       |
| Concentração máx. por segmento       | Semanal        | Sistema de gestão de carteira             | 🟡 28% Logística         | Gestor              |
| Caixa disponível                     | Diário         | Conta corrente do fundo + títulos DI      | 🟢 4,1% do PL            | Administrador       |

> 📎 **Fonte:** Práticas de mercado: relatórios de gestão de risco de FoFs de referência (BCFF11, RBRF11, HGFF11 — relatórios públicos CVM)

## 6.4 Risco de Crédito — Locatário (FII de Tijolo)
A análise de risco do locatário é uma das competências mais críticas do gestor de FII de tijolo. Um locatário em dificuldade financeira pode deixar de pagar aluguel, pedir para rescindir ou renegociar abaixo do mercado — gerando impacto direto e duradouro no DY do fundo.

| **Indicador do Locatário**           | **Threshold de Atenção**                | **Fonte de Dados**                           | **Frequência de Monitoramento**     |
|--------------------------------------|-----------------------------------------|----------------------------------------------|-------------------------------------|
| EBITDA / Aluguel Anual (cobertura)   | \< 3,0x → atenção; \< 2,0x → alarme     | DRE pública (se listado) ou relatório do FII | Trimestral (resultado do locatário) |
| Dívida Líquida / EBITDA              | Corporates: \> 3,5x; Varejo: \> 2,5x    | Relatório de resultados; agencies de rating  | Trimestral                          |
| Rating de crédito do locatário       | Rebaixamento abaixo de BBB-/brBBB-      | Fitch, S&P, Moody's; ANBIMA                  | Contínuo (alertas automáticos)      |
| Inadimplência de aluguel (dias)      | 30+ dias → atenção; 60+ dias → ação     | Relatório gerencial do FII                   | Mensal                              |
| Prazo remanescente do contrato       | \< 18 meses → risco de vacância próximo | Contrato de locação; relatório do FII        | Mensal                              |
| Percentual da receita em 1 locatário | Mono-inquilino \> 80%                   | Relatório do FII                             | Mensal                              |

> 📎 **Fonte:** Moody's Local — Metodologia de Rating de FIIs (2024); Fitch Ratings — FII Rating Criteria Brasil (2024)

## 6.5 Risco de Juros e Sensibilidade (FII de Papel)
FIIs de papel são essencialmente fundos de renda fixa com benefício fiscal. A principal dimensão de risco é a sensibilidade à taxa de juros — especialmente para CRIs IPCA+ com prazo longo:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>📐 Cálculo de DV01 e Duration para Carteira de CRIs</strong></td>
</tr>
<tr class="even">
<td><p>Duration de Macaulay = Σ[t × (FC_t / (1+r)^t)] / Preço</p>
<p>Modified Duration = Duration / (1 + r)</p>
<p>DV01 = Modified Duration × Valor da Posição × 0,0001 (1 bp)</p>
<p>Exemplo: CRI IPCA+ 2030 com Modified Duration 4,5 anos e posição R$ 100M</p>
<p>DV01 = 4,5 × R$100M × 0,0001 = R$ 45.000 por bp de variação na NTN-B</p>
<p>Carteira com Duration 5,2 anos: alta de 100 bps na NTN-B → perda estimada de ~5,2% no valor da carteira</p></td>
</tr>
</tbody>
</table>

> 📎 **Fonte:** CFA Institute — Fixed Income Analysis (2024); Tesouro Nacional — Metodologia de Duration da Dívida Pública

| **Cenário de Juros**            | **Impacto Estimado no FII de Papel IPCA+**             | **Impacto no FII de Papel CDI+**                        | **Ação de Mitigação**                             |
|---------------------------------|--------------------------------------------------------|---------------------------------------------------------|---------------------------------------------------|
| Alta de 100 bps (NTN-B)         | Queda de ~3–6% no NAV da carteira (varia por duration) | Efeito positivo no DY; NAV relativamente estável        | Reduzir duration; aumentar CDI+ vs. IPCA+         |
| Alta de 200 bps (NTN-B)         | Queda de ~6–12% no NAV da carteira                     | DY sobe; investidores tendem a resgatar (se aberto)     | Hedge de duration via NTN-B vendida               |
| Queda de 100 bps (NTN-B)        | Alta de ~3–6% no NAV; valorização de carteira          | DY cai; possível saída de cotistas por retorno absoluto | Aumentar duration; travar spreads altos           |
| Inflação IPCA acima do esperado | Positivo: principal e juros corrigidos pelo IPCA       | Neutro (CDI+ já captura via Selic)                      | Manter alocação em IPCA+ como hedge inflacionário |

> 📎 **Fonte:** Banco Central do Brasil — Relatório de Estabilidade Financeira (2024); NTN-B Tesouro Nacional (tesouro.gov.br)

## 6.6 Plano de Contingência e Stress Test — FII
O stress test é o exercício de simular cenários adversos para verificar se o fundo consegue honrar seus compromissos e manter a integridade da carteira. Para FIIs, os principais cenários de estresse a testar são:

| **Cenário de Estresse**                       | **Premissa**                                | **Impacto Esperado**                                  | **Ação de Mitigação**                             |
|-----------------------------------------------|---------------------------------------------|-------------------------------------------------------|---------------------------------------------------|
| Crise de liquidez de mercado                  | ADV cai 70%; spread bid/ask triplica        | Impossibilidade de liquidar \>20% do PL em 30 dias    | Manter caixa mínimo; portfólio com ADV adequado   |
| Alta abrupta de juros (+300 bps)              | NTN-B salta 300 bps em 3 meses              | NAV cai 10–18% (papel IPCA+); cotistas pedem resgate  | Hedge parcial de duration; limite de resgate      |
| Recessão profunda com alta vacância           | Vacância salta de 8% para 25% no segmento   | Queda de 20–30% no DY; risco de inadimplência         | Diversificação; contratos atípicos; covenants     |
| Default de locatário âncora                   | Maior locatário (30% receita) para de pagar | Perda imediata de 30% da receita; valor do imóvel cai | Diversificação por locatário; cobertura de seguro |
| Mudança regulatória — perda de isenção fiscal | Isenção de IR revogada para PF              | Queda de preços de mercado de 15–25% nos FIIs         | Monitoramento legislativo; estruturação robusta   |

> 📎 **Fonte:** Banco Central do Brasil — Nota de Estabilidade Financeira; CVM — Orientação sobre Testes de Estresse em FIs (2023)

---

# PARTE III
## FUNDO DE INVESTIMENTO EM DIREITOS CREDITÓRIOS — FIDC
*Análise de Crédito, Modelagem e Monitoramento Operacional*
# 7. Análise de Crédito e Originação no FIDC
O mercado de FIDCs no Brasil movimenta mais de R$ 450 bilhões em patrimônio líquido (dados CVM/ANBIMA 2024), posicionando o veículo como um dos pilares do crédito privado nacional. A competência central do gestor é a análise de crédito do cedente e dos devedores — antes da estruturação e de forma contínua após o início das operações.

> 📎 **Fonte:** CVM — Painel de Fundos de Investimento — FIDC (dados.cvm.gov.br, 2025); ANBIMA — Boletim de Fundos Estruturados Q4/2024

## 7.1 Análise do Cedente
| **Dimensão**              | **O Que Verificar**                                                               | **Ferramentas / Fontes**                                  |
|---------------------------|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| Saúde Financeira          | DRE, Balanço, Fluxo de Caixa 3 anos auditados; covenants bancários; endividamento | Balanços auditados; SCR Bacen; debêntures / CRIs emitidos |
| Qualidade da Originação   | Processo de concessão; histórico de inadimplência própria; taxa de aprovação      | Data room do cedente; entrevista com equipe de crédito    |
| Concentração de Carteira  | % dos 10 maiores devedores; exposição setorial; risco geográfico                  | Base de dados da carteira (sample ou completa)            |
| Sistemas Operacionais     | Geração de arquivo de cessão; integração com custodiante; controle de baixas      | Demo do sistema; piloto de cessão                         |
| Histórico de FIDC         | Cedente já operou FIDC? Com quem? Saiu bem? Houve defaults?                       | Consulta ao mercado; relatórios CVM de FIDCs existentes   |
| Compliance e Regularidade | Certidões negativas; litígios; processos trabalhistas; regulatório setorial       | Certidões cartorárias; Bacen; CVM; Receita Federal        |

> 📎 **Fonte:** Banco Central do Brasil — SCR (Sistema de Informações de Crédito, bcb.gov.br/estabilidadefinanceira/scr); Fitch Ratings — Metodologia de FIDC Brasil (2024)

## 7.2 Análise de Vintages
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>📊 Como Interpretar a Análise de Vintages</strong></td>
</tr>
<tr class="even">
<td><p>Eixo X: meses desde a originação (0, 3, 6, 9, 12, 18, 24+)</p>
<p>Eixo Y: taxa de inadimplência acumulada (% sobre volume originado no vintage)</p>
<p>O que observar:</p>
<p>• Forma da curva: côncava (acelera no início) vs. convexa (piora no longo prazo)</p>
<p>• Plateau: onde a inadimplência estabiliza (taxa final de perda por coorte)</p>
<p>• Tendência entre vintages: safras recentes piores = deterioração de originação</p>
<p>• Sazonalidade: períodos consistentemente piores (jan, jul — pós-férias)</p>
<p>• Divergência em anos de crise (2020, 2022) vs. anos normais</p></td>
</tr>
</tbody>
</table>

> 📎 **Fonte:** Fitch Ratings — Structured Finance Criteria: FIDC Brasil (2024); Moody's Local — Metodologia de FIDC (2023)

## 7.3 Modelagem e Precificação
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>📐 Fórmula de Precificação Mínima dos Recebíveis</strong></td>
</tr>
<tr class="even">
<td><p>Taxa Mínima = Custo das Cotas Sênior + Perda Esperada + Custo Operacional + Spread Subordinada</p>
<p>Exemplo — FIDC de duplicatas:</p>
<p>• Custo das cotas sênior: CDI + 1,8% a.a.</p>
<p>• Perda esperada: 4,0% a.a. (base vintages + margem 30%)</p>
<p>• Custo operacional (admin + gestão + custódia + auditoria): 1,2% a.a.</p>
<p>• Spread para cotas subordinadas: 3,0% a.a.</p>
<p>→ Taxa mínima de desconto = CDI + 10,0% a.a.</p></td>
</tr>
</tbody>
</table>

> 📎 **Fonte:** ANBIMA — Manual de Precificação de Ativos de Crédito (MtM, 2024); Fitch Ratings — FIDC Criteria

# 8. Monitoramento Operacional do FIDC
## 8.1 Dashboard de Monitoramento
| **Indicador**            | **Frequência** | **Alerta Amarelo**            | **Alerta Vermelho**         | **Ação**                                                    |
|--------------------------|----------------|-------------------------------|-----------------------------|-------------------------------------------------------------|
| Inadimplência 30+ dias   | Diária         | \> 80% do limite regulamentar | \> limite — covenant breach | Comitê; notificar administrador; avaliar early amortization |
| Índice de subordinação   | Diária         | \< índice mín. + 200 bps      | \< índice mínimo            | Suspender cessões; plano de recomposição                    |
| Volume de cessão diária  | Diária         | \< 70% do target acumulado    | \< 50% do target            | Reunião com cedente; avaliar capacidade de originação       |
| WAL (prazo médio)        | Semanal        | Desvio \> 15% do target       | Desvio \> 25%               | Revisão dos critérios de elegibilidade de prazo             |
| Concentração por devedor | Semanal        | \> 80% do limite por devedor  | \> limite                   | Bloquear novas cessões; notificar custodiante               |
| Saldo de caixa           | Diária         | \< 3% do PL                   | \< 1,5% do PL               | Revisão do calendário de amortização                        |

> 📎 **Fonte:** CVM — Resolução 175/2022, Anexo I (FIDC); Resolução BCB 29/2020 (deveres do custodiante)

---

# MÓDULO DE RISCO — FIDC
## Controle e Gestão de Risco para Fundos de Direitos Creditórios
# 9. Controle e Gestão de Risco — FIDC
O FIDC concentra riscos de crédito, operacional, legal e de liquidez de forma mais intensa do que qualquer outro veículo de fundos estruturados. O gestor deve operar com três camadas de controle simultaneamente: o monitoramento da carteira de crédito, o controle da estrutura do fundo (índices e covenants) e a vigilância sobre o cedente e o custodiante.

> 📎 **Fonte:** CVM — Resolução 175/2022, Anexo I; Fitch Ratings — FIDC Rating Criteria (2024); ANBIMA — Código ART 2023

## 9.1 Taxonomia de Riscos do FIDC
| **Categoria**         | **Subcategoria**                 | **Fonte do Risco**                                           | **Impacto Potencial**                                           |
|-----------------------|----------------------------------|--------------------------------------------------------------|-----------------------------------------------------------------|
| Risco de Crédito      | Inadimplência dos devedores      | Deterioração financeira dos sacados; fraude; ciclo econômico | Perda direta no patrimônio; breach do índice de subordinação    |
| Risco de Crédito      | Risco do cedente (coobrigação)   | Insolvência do cedente em estrutura com coobrigação          | Acionamento da coobrigação; concentração do risco no cedente    |
| Risco de Concentração | Por devedor                      | Exposição excessiva a um único sacado                        | Evento único derruba o índice de subordinação                   |
| Risco de Concentração | Por setor                        | Carteira concentrada num setor correlacionado                | Choque setorial impacta toda a carteira                         |
| Risco Operacional     | Cessão de crédito inválida       | Falha no processo de verificação de elegibilidade            | Crédito inelegível na carteira; responsabilidade do custodiante |
| Risco Legal           | Invalidade da cessão             | Questionamento judicial da cessão; cessão não registrada     | Reintegração do crédito ao patrimônio do cedente (falência)     |
| Risco de Estrutura    | Breach de índice de subordinação | Inadimplência ou amortização abaixo do esperado              | Acionamento de early amortization; perda para cotas sênior      |
| Risco de Liquidez     | Descasamento de prazos           | Créditos de longo prazo vs. cotas com amortização curta      | Incapacidade de pagar cotas sênior no vencimento                |
| Risco Operacional     | Fraude na originação             | Créditos fictícios cedidos ao fundo                          | Perda total dos créditos fraudados; responsabilização           |

> 📎 **Fonte:** Fitch Ratings — Global Structured Finance Rating Criteria (2024); CVM — Parecer de Orientação CVM/SIN sobre FIDC

## 9.2 Sistema de Limites Operacionais — FIDC
| **Parâmetro**                 | **Limite Típico de Mercado**              | **Alerta**          | **Ação**                                                     |
|-------------------------------|-------------------------------------------|---------------------|--------------------------------------------------------------|
| Índice de subordinação mínimo | Definido no regulamento (ex.: 15%)        | \< mínimo + 300 bps | Suspender novas cessões; plano de recomposição em 30 dias    |
| Inadimplência 30+ dias        | Ex.: máx 6% da carteira                   | 80% do limite       | Comitê de crise; revisão dos critérios de elegibilidade      |
| Inadimplência 90+ dias        | Ex.: máx 4% da carteira                   | 80% do limite       | Acionar early amortization se mantido por 3 dias             |
| Concentração por devedor      | Ex.: máx 5% do PL                         | 80% do limite       | Bloquear cessões desse devedor                               |
| Concentração por setor        | Ex.: máx 30% do PL                        | 85% do limite       | Revisão estratégica; não aprovar novas cessões do setor      |
| WAL máximo da carteira        | Ex.: 180 dias                             | Desvio \> 20%       | Revisar elegibilidade de prazo; não aceitar créditos longos  |
| Índice de cobertura (IC)      | IC = Ativo total / Passivo sênior ≥ 1,20x | IC \< 1,25x         | Reunião de emergência; avaliar emissão de cotas subordinadas |
| Taxa de recuperação observada | \> 40% dos créditos inadimplentes         | \< 40% por 2 meses  | Revisar processo de cobrança; substituir empresa de cobrança |

> 📎 **Fonte:** Moody's Local — Metodologia de FIDC Brasil (2023); Fitch Ratings — FIDC Criteria; CVM Res. 175/2022 Anexo I

## 9.3 Processo de Early Amortization (Amortização Antecipada)
O evento de amortização antecipada (early amortization) é o mecanismo de proteção final dos cotistas sênior. Deve estar previsto com precisão no regulamento do fundo, com gatilhos objetivos e mensuráveis. A ambiguidade nos gatilhos é uma das principais fontes de litígio em FIDCs em dificuldade.

| **Tipo de Gatilho**          | **Exemplo de Parâmetro**                                     | **Consequência**                                                   | **Documentação Necessária**                                            |
|------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------|------------------------------------------------------------------------|
| Quantitativo — Inadimplência | Inadimplência 90+ dias \> 6% por 3 dias úteis consecutivos   | Suspensão de novas cessões; início de amortização das cotas sênior | Cálculo diário do índice pelo custodiante; comunicado ao administrador |
| Quantitativo — Subordinação  | Índice de subordinação \< 12% por qualquer dia               | Suspensão imediata de cessões; convocação de assembleia em 15 dias | Cálculo diário pelo custodiante; protocolo de notificação              |
| Qualitativo — Cedente        | Intervenção, liquidação extrajudicial ou falência do cedente | Rescisão do contrato de cessão; aceleração total                   | Monitoramento diário do status legal do cedente (DJE, CVM, Bacen)      |
| Qualitativo — Estrutura      | Rebaixamento das cotas sênior abaixo do grau de investimento | Obrigação de recomposição em 60 dias ou early amortization         | Alerta automático da agência de rating; notificação ao administrador   |
| Qualitativo — Fraude         | Descoberta de créditos fictícios ou irregulares na carteira  | Early amortization imediata; acionamento de garantias              | Due diligence forense; advogados contratados pelo fundo                |
| Qualitativo — Operacional    | Custodiante ou administrador perdem autorização CVM/Bacen    | Substituição em 90 dias; se não houver, early amortization         | Monitoramento do status regulatório dos prestadores de serviço         |

> 📎 **Fonte:** CVM — Resolução 175/2022, Anexo I, Art. 20 a 28 (eventos de liquidação); Fitch Ratings — FIDC Criteria; modelos de regulamento de mercado

## 9.4 Auditoria de Carteira e Verificação de Elegibilidade
A auditoria de carteira é um controle preventivo essencial que vai além da verificação rotineira do custodiante. O gestor deve contratar periodicamente auditoria independente dos créditos cedidos para verificar a validade, existência e exigibilidade dos recebíveis da carteira.

| **Tipo de Auditoria**                    | **Frequência**         | **Escopo**                                                                 | **Executor**                                              |
|------------------------------------------|------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| Verificação de elegibilidade (rotineira) | A cada cessão          | Checagem dos critérios do regulamento para os créditos da cessão           | Custodiante (obrigatório pela Res. BCB 29/2020)           |
| Auditoria de amostragem (carteira)       | Trimestral             | Amostra de 5–10% da carteira; verificar existência e validade dos créditos | Empresa de auditoria contratada pelo gestor               |
| Auditoria forense (evento específico)    | Quando houver suspeita | 100% ou amostra ampla; investigação de irregularidades                     | Auditoria especializada em forensics                      |
| Revisão dos processos do cedente         | Semestral              | Avaliação do processo de originação, aprovação e cessão                    | Gestor + equipe de risco; eventualmente auditoria externa |
| Auditoria das demonstrações do fundo     | Anual (obrigatório)    | DRE, balanço, carteira consolidada, notas explicativas                     | Auditor independente registrado na CVM                    |

> 📎 **Fonte:** Resolução BCB 29/2020 (deveres do custodiante); CVM Res. 175/2022, Art. 71 (auditoria independente); PCAOB / CFC NBC TA 700

## 9.5 Matriz de Responsabilidades no Controle de Risco — FIDC
| **Atividade de Controle**                | **Gestor**                   | **Administrador**        | **Custodiante**            | **Auditor**     |
|------------------------------------------|------------------------------|--------------------------|----------------------------|-----------------|
| Verificação de elegibilidade da cessão   | Aprovação                    | Supervisão               | Execução (primária)        | —               |
| Cálculo diário do índice de subordinação | Monitoramento                | Validação                | Cálculo (primário)         | —               |
| Monitoramento de inadimplência           | Análise e decisão            | Reporte regulatório      | Apuração diária            | Validação anual |
| Acionamento de early amortization        | Proposta e decisão           | Notificação formal à CVM | Suspensão de novas cessões | —               |
| Auditoria da carteira de créditos        | Contratação e acompanhamento | Co-supervisão            | Fornecimento de dados      | Execução        |
| Relatório mensal ao cotista              | Elaboração e envio           | Revisão regulatória      | Dados operacionais         | —               |
| Marcação a mercado dos créditos          | Metodologia e aprovação      | Validação                | Aplicação diária           | Revisão anual   |
| Monitoramento do cedente                 | Análise contínua             | Registro de eventos      | —                          | —               |

> 📎 **Fonte:** CVM — Resolução 175/2022 (responsabilidades dos participantes); Resolução BCB 29/2020; ANBIMA Código ART 2023

---

# PARTE IV
## FIAGRO — FUNDOS DO AGRONEGÓCIO
*Análise de Crédito Rural, Teses de Investimento e Gestão Ativa*
# 10. Análise de Investimentos no FIAGRO
O agronegócio representa 25–27% do PIB brasileiro e necessita de financiamento superior a R$ 500 bilhões por safra, grande parte ainda dependente do crédito público rural. O FIAGRO — criado pela Lei 14.130/2021 — é o veículo que conecta esse gap ao mercado de capitais, com benefício fiscal análogo ao FII.

> 📎 **Fonte:** CEPEA/USP — Relatório PIB do Agronegócio Brasil 2024; MAPA — Plano Safra 2024/2025; Lei nº 14.130/2021

## 10.1 Framework de Análise de CRA
| **Camada**               | **O que Analisar**                                                              | **Sinais de Alerta**                                       |
|--------------------------|---------------------------------------------------------------------------------|------------------------------------------------------------|
| Emissor (Securitizadora) | Track record, experiência em agro, PL, governance                               | Securitizadora genérica sem especialização; baixo PL       |
| Devedor Principal        | Produtor, trading, processadora, cooperativa — porte e histórico                | Produtor individual sem escala; trading alavancado         |
| Lastro                   | CPR, contrato comercial, nota de crédito rural — qual a garantia real?          | Expectativa de produção sem hedge ou seguro                |
| Garantias                | Imóvel rural (hipoteca/AF), estoques, aval, seguro agrícola                     | LTV rural \> 50% sem reforço de garantia                   |
| Covenants                | Índices financeiros, obrigações de informação, eventos de vencimento antecipado | Poucos ou nenhum covenant; ausência de reporte obrigatório |
| Rating                   | Rating da emissão e do devedor; agência; data                                   | Rating \> 18 meses; agência sem especialização em agro     |

> 📎 **Fonte:** ANBIMA — Informe de CRAs 2024; Moody's Local — Metodologia de Rating de CRAs (2023); Lei 11.076/2004

## 10.2 Due Diligence Fundiária
| **Documento**                 | **Onde Obter**                               | **O Que Valida**                                        |
|-------------------------------|----------------------------------------------|---------------------------------------------------------|
| Matrícula do imóvel           | Cartório de Registro de Imóveis (comarca)    | Proprietário, ônus reais, histórico de alienações       |
| CCIR                          | Incra / Portal Incra (incra.gov.br)          | Cadastro federal; área declarada ao Incra               |
| ITR                           | Receita Federal (receita.fazenda.gov.br)     | Regularidade fiscal; área para fins tributários         |
| CAR                           | SICAR / SeMAS estaduais (car.gov.br)         | Reserva Legal, APP, uso e cobertura da terra            |
| Georreferenciamento SIGEF     | Incra/SIGEF (sigef.incra.gov.br)             | Coordenadas certificadas; sobreposição com outras áreas |
| Sobreposições (FUNAI, ICMBio) | Funai / ICMBio / Incra (assentamentos)       | Terras indígenas, UCs, assentamentos                    |
| PRODES / Deter                | INPE — TerraBrasilis (terrabrasilis.inpe.br) | Histórico de desmatamento; alertas ativos               |
| Embargos IBAMA                | IBAMA / SINAFLOR (ibama.gov.br)              | Sanções ambientais; embargos ativos ou históricos       |

> 📎 **Fonte:** INCRA — Manual de Georreferenciamento de Imóveis Rurais (2024); MAPA — Instrução Normativa CAR; IBAMA — Manual de Fiscalização

---

# MÓDULO DE RISCO — FIAGRO
## Controle e Gestão de Risco para Fundos do Agronegócio
# 11. Controle e Gestão de Risco — FIAGRO
O FIAGRO acumula riscos únicos que não existem em FIIs ou FIDCs convencionais: risco agropecuário (climático, de produção, de preço de commodity), risco fundiário (titulação, regularidade ambiental, sobreposições), risco de câmbio (via commodities) e risco de ESG regulatório (desmatamento, trabalho escravo, passivo ambiental). O gestor de FIAGRO precisa de um framework de risco multidimensional específico para o setor.

> 📎 **Fonte:** MAPA — Plano ABC+ 2020–2030; IBGE — Censo Agropecuário 2017 (referência estrutural); CVM Res. 175/2022 Anexo IV

## 11.1 Taxonomia de Riscos do FIAGRO
| **Categoria**      | **Subcategoria**              | **Fonte do Risco**                                         | **Instrumento de Medição**                            |
|--------------------|-------------------------------|------------------------------------------------------------|-------------------------------------------------------|
| Risco Agropecuário | Risco de produção             | Clima (seca, geada, excesso de chuva), pragas, doenças     | Zarc/MAPA; histórico de produtividade; laudo agrônomo |
| Risco Agropecuário | Risco de preço de commodity   | Ciclo global de preços (soja, milho, boi); BRL/USD         | Curva de futuros B3/CME; índices ESALQ; Cepea         |
| Risco Fundiário    | Titulação irregular           | Sobreposição com TI, UC, assentamento; cadeia dominial     | SIGEF/Incra; FUNAI; ICMBio; análise jurídica          |
| Risco Ambiental    | Passivo ambiental             | Desmatamento ilegal, APP/RL irregular, embargo IBAMA       | PRODES/INPE; CAR/SICAR; IBAMA                         |
| Risco de Crédito   | Inadimplência do produtor     | Frustração de safra; queda de preço; sobreendividamento    | SCR Bacen; vintages de inadimplência; score rural     |
| Risco de Liquidez  | Imóvel rural (tijolo)         | Mercado imobiliário rural ilíquido; localização remota     | Prazo estimado de venda; cap rate rural de saída      |
| Risco ESG          | Trabalho análogo ao escravo   | Fiscalização SRTE/MTE; cadeia de fornecedores              | Lista Suja MTE; auditorias trabalhistas               |
| Risco ESG          | Desmatamento ilegal           | Nova legislação florestal; compliance com Código Florestal | PRODES; Deter/INPE; certificações (RA, RTRS)          |
| Risco Regulatório  | Mudança na legislação do agro | Reforma do Código Florestal; PL tributário                 | Monitoramento legislativo; buffers de estrutura       |

> 📎 **Fonte:** MAPA — Zoneamento Agrícola de Risco Climático (Zarc); INPE — TerraBrasilis; BCB — SCR; MTE — Lista de Empregadores com Trabalho Escravo

## 11.2 Sistema de Limites — FIAGRO
| **Parâmetro**                         | **Limite Recomendado**                               | **Alerta**      | **Ação Requerida**                                    |
|---------------------------------------|------------------------------------------------------|-----------------|-------------------------------------------------------|
| Concentração por cultura              | Máx. 40% do PL em uma cultura                        | ≥ 35%           | Diversificar entre culturas; reduzir exposição        |
| Concentração por região               | Máx. 35% do PL em uma macrorregião                   | ≥ 30%           | Diversificar geograficamente; limitar novas operações |
| Concentração por devedor (crédito)    | Máx. 10% do PL num único devedor                     | ≥ 8%            | Bloquear novas operações com o devedor                |
| LTV de imóvel rural                   | Máx. 50% (conservador); máx. 65% com aval            | ≥ 45% sem aval  | Exigir garantias complementares                       |
| Cobertura de seguro agrícola          | Mín. 70% do volume financiado                        | \< 75%          | Exigir ampliação da cobertura antes de nova cessão    |
| Prazo médio da carteira               | Compatível com o calendário agrícola (máx. 2 safras) | Desvio \> 30%   | Revisar critérios de elegibilidade de prazo           |
| Exposição a produtores sem CAR ativo  | 0% (exclusão total)                                  | Qualquer caso   | Não aprovar; notificar administrador                  |
| Exposição a imóveis com embargo IBAMA | 0% (exclusão total)                                  | Qualquer alerta | Bloquear imóvel; providências jurídicas               |

> 📎 **Fonte:** MAPA — Resolução BNDES/Pronaf; BCB — Resolução CMN 4.901/2021 (crédito rural); IBAMA — Lista de Embargos Ambientais

## 11.3 Dashboard de Risco — FIAGRO
| **Indicador**                           | **Frequência** | **Fonte de Dados**                                       | **Ação em Caso de Alerta**                                          |
|-----------------------------------------|----------------|----------------------------------------------------------|---------------------------------------------------------------------|
| Alerta de desmatamento nas fazendas     | Diário/Semanal | INPE — Deter / TerraBrasilis (gratuito, API disponível)  | Verificar imóvel; comunicar ao administrador; análise jurídica      |
| Preço das commodities financiadas       | Diário         | ESALQ/CEPEA; CME Group; B3 (futuros de soja, milho)      | Avaliar cobertura de preço; verificar hedge dos devedores           |
| BRL/USD (câmbio)                        | Diário         | Banco Central; Bloomberg; Reuters                        | Avaliar impacto na capacidade de pagamento de exportadores          |
| Boletim climático (regiões da carteira) | Semanal        | INMET; Climatempo; Embrapa (informes agrometeorológicos) | Alertar sobre risco de frustração de safra; acionar seguro          |
| Zarc — Zoneamento de Risco (pré-cessão) | Por cessão     | MAPA — Portal Zarc (zarc.mapa.gov.br)                    | Não aprovar crédito em municípios fora do zoneamento da cultura     |
| Inadimplência da carteira               | Mensal         | Custodiante; relatório de cedente                        | Acionar cobrança; revisar critérios se tendência                    |
| Status CAR dos imóveis (novo)           | Semestral      | SICAR / SeMAS estaduais                                  | Se CAR cancelado ou suspenso: bloquear novas operações com o imóvel |
| Lista Suja MTE (trabalho escravo)       | Mensal         | MTE — Portal Lista Suja (sit.trabalho.gov.br)            | Se devedor listado: vencimento antecipado; desinvestimento          |

> 📎 **Fonte:** INPE — TerraBrasilis API (terrabrasilis.inpe.br); MAPA — Portal Zarc; MTE — Portaria 1.293/2017 (Lista Suja); SICAR/Car.gov.br

## 11.4 Risco de Produção — Análise por Cultura
| **Cultura**      | **Risco Climático Principal**            | **Região de Maior Risco**               | **Seguro Disponível**                      | **Período Crítico**                      |
|------------------|------------------------------------------|-----------------------------------------|--------------------------------------------|------------------------------------------|
| Soja (1ª safra)  | Veranico; excesso de chuva na colheita   | MATOPIBA (seca); PR/RS (chuva colheita) | ProAgro / privado (SoCo, Tokio, BB Mapfre) | Fev–Abr (enchimento de grãos e colheita) |
| Milho (safrinha) | Geada; veranico após plantio tardio      | PR/SP/MG (geada); MT/MS (veranico)      | ProAgro / privado                          | Jul–Set (enchimento de grãos no inverno) |
| Café (Arábica)   | Geada; seca prolongada; bienalidade      | MG Sul; SP Mogiana; ES Montanhas        | Privado (poucos; mercado restrito)         | Jun–Jul (florada e granação)             |
| Cana-de-Açúcar   | Seca na fase de crescimento; queimadas   | SP Centro-Sul; NE (seca)                | Privado + hedge de açúcar/etanol           | Set–Nov (maturação e início de colheita) |
| Algodão          | Excesso de chuva na colheita; pragas     | BA/MA/MT (Cerrado)                      | ProAgro / privado                          | Jan–Mar (colheita)                       |
| Boi Gordo        | Seca (pastagens); doenças (febre aftosa) | Pantanal; MS; GO (seca)                 | Seguro pecuário privado (limitado)         | Mai–Out (seca; confinamento necessário)  |

> 📎 **Fonte:** MAPA — Zarc por Município e Cultura (2024); EMBRAPA — Boletim de Pesquisa Agropecuária; INMET — Climatologia

## 11.5 Gestão de Risco ESG no FIAGRO
O risco ESG no FIAGRO é simultaneamente um risco reputacional, um risco regulatório e um risco financeiro direto — propriedades com passivo ambiental não têm valor de garantia adequado e devedores com embargo não podem comercializar sua produção. O gestor que ignora ESG assume riscos financeiros concretos.

| **Dimensão ESG**                 | **Risco Financeiro Associado**                                                 | **Indicador de Monitoramento**                               | **Fonte**                            |
|----------------------------------|--------------------------------------------------------------------------------|--------------------------------------------------------------|--------------------------------------|
| E — Desmatamento ilegal          | Garantia (imóvel) desvalorizada; embargo bloqueia venda; risco de reintegração | Alertas PRODES/Deter; % de imóveis com embargo               | INPE TerraBrasilis; IBAMA            |
| E — APP/RL irregular             | Nulidade do CAR; risco de execução de garantia contestada                      | Status CAR: ativo, pendente, cancelado                       | SICAR; Cadastro CVM das propriedades |
| E — Uso de agrotóxicos proibidos | Embargo da produção; impossibilidade de exportação                             | Certificação de conformidade; lista de agrotóxicos proibidos | MAPA; ANVISA; IBAMA                  |
| S — Trabalho análogo ao escravo  | Vencimento antecipado obrigatório; responsabilidade solidária                  | Lista Suja MTE atualizada mensalmente                        | MTE (sit.trabalho.gov.br)            |
| S — Condições de trabalho rural  | Multas SRTE; embargo da atividade; risco reputacional                          | Relatório de auditorias trabalhistas; certidões MTE          | MTE; E-Social                        |
| G — Governança do devedor        | Risco de fraude na originação; inadimplência por gestão deficiente             | Demonstrações auditadas; análise de partes relacionadas      | CVM; balanços auditados              |

> 📎 **Fonte:** MAPA — Plano ABC+ 2020–2030; INPE — Monitoramento do Desmatamento; MTE — Portaria 1.293/2017; CVM Res. 59/2022 (ESG)

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>🌿 Checklist ESG Mínimo para Aprovação de Crédito no FIAGRO</strong></td>
</tr>
<tr class="even">
<td><p>□ CAR ativo e sem pendências — verificado no SICAR (car.gov.br)</p>
<p>□ Ausência de embargos IBAMA ativos — verificado no SINAFLOR (ibama.gov.br)</p>
<p>□ Ausência na Lista Suja do MTE — verificado em sit.trabalho.gov.br</p>
<p>□ PRODES — sem alerta de desmatamento nos últimos 24 meses — TerraBrasilis</p>
<p>□ CCIR regular e ITR quitado — Incra e Receita Federal</p>
<p>□ Cobertura de seguro agrícola confirmada — apólice vigente para a safra</p>
<p>□ Zarc favorável para a cultura e município — MAPA/Zarc</p>
<p>□ Laudo técnico de engenheiro agrônomo (produtividade e práticas agronômicas)</p>
<p>Ausência de qualquer item = crédito bloqueado para cessão até regularização</p></td>
</tr>
</tbody>
</table>

> 📎 **Fonte:** MAPA — Zoneamento Agrícola; IBAMA; INPE; MTE — portarias vigentes; CVM Resolução 175/2022 Anexo IV

---

# PARTE V
## ESTRUTURAÇÃO DE PRODUTOS E ECOSSISTEMA
# 12. Estruturação de Produtos — Do Conceito à Distribuição
## 12.1 Jornada de Estruturação
| **Fase**                   | **Duração** | **Entregas**                                         | **Quem Lidera**                  |
|----------------------------|-------------|------------------------------------------------------|----------------------------------|
| 1\. Concepção              | 2–4 sem     | Briefing; análise de viabilidade; estrutura proposta | Especialista de Produto + Gestor |
| 2\. Estruturação Jurídica  | 4–8 sem     | Regulamento; contratos; opinião legal                | Advogados + Administrador        |
| 3\. Due Diligence          | 4–12 sem    | Laudos; análise de crédito; modelos financeiros      | Gestor + Consultores             |
| 4\. Modelagem Financeira   | 2–4 sem     | Fluxo de caixa; sensibilidades; retorno por classe   | Gestor + Produto                 |
| 5\. Rating (se aplicável)  | 4–8 sem     | Data room; rating preliminar; ajustes estruturais    | Gestor + Agência                 |
| 6\. Registro CVM           | 4–8 sem     | Protocolo; análise CVM; exigências; deferimento      | Administrador + Advogados        |
| 7\. Preparação Comercial   | 2–4 sem     | Teaser; deck; due diligence package                  | Produto + Distribuição           |
| 8\. Distribuição           | 2–6 sem     | Roadshow; bookbuilding; subscrições                  | Coordenador + Distribuição       |
| 9\. Monitoramento contínuo | Permanente  | Gestão da carteira; relatórios; assembleias          | Gestor + Administrador           |

> 📎 **Fonte:** CVM — Resolução 175/2022 (registro de fundos); CVM — Resolução 160/2022 (distribuição pública); ANBIMA — Código de Processos de Elegibilidade

## 12.2 Gestão de Conflitos de Interesse no Ecossistema
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>⚠️ Situações que Exigem Protocolo Formal de Conflito de Interesse</strong></td>
</tr>
<tr class="even">
<td><p>• Aquisição pelo FII de imóvel de empresa do mesmo grupo do gestor ou administrador</p>
<p>• FIDC comprando créditos originados por empresa do grupo financeiro controlador da gestora</p>
<p>• Contratação de prestador indicado por cotista relevante sem processo competitivo</p>
<p>• Gestor ou sócio que é acionista do cedente do FIDC</p>
<p>• Follow-on de FII em que a gestora também é incorporadora/vendedora dos ativos</p>
<p>Em todos os casos: documentar o processo; obter fairness opinion independente; submeter à assembleia quando exigido</p></td>
</tr>
</tbody>
</table>

> 📎 **Fonte:** CVM — Resolução 175/2022, Arts. 40–45 (conflito de interesse); ANBIMA — Código ART, Seção 4

---

# PARTE VI
## MACRO, ROTINAS E GESTÃO INTEGRADA DE RISCO
# 13. Ambiente Macroeconômico e Rotinas Operacionais
## 13.1 Impacto dos Juros nos Três Veículos
| **Cenário**               | **FII Tijolo**                                 | **FII Papel**                                       | **FIDC**                                             | **FIAGRO**                                                      |
|---------------------------|------------------------------------------------|-----------------------------------------------------|------------------------------------------------------|-----------------------------------------------------------------|
| Alta de juros (+100 bps)  | Negativo: P/VP cai; custo de oportunidade sobe | Positivo: DY CDI+ sobe em termos absolutos          | Neutro a positivo: retorno bruto sobe                | Misto: CDI sobe; câmbio pode apreciar (bom exportador)          |
| Queda de juros (-100 bps) | Positivo: re-rating; P/VP sobe                 | Negativo: DY absoluto cai                           | Negativo: spread CDI+ comprime em novas emissões     | Misto: câmbio pode depreciar (ruim p/ importadores de insumos)  |
| Inflação alta (IPCA)      | Positivo: reajuste real dos contratos IPCA     | Muito positivo: CRIs IPCA+ entregam retorno real    | Neutro (CDI geralmente)                              | Positivo: CRAs IPCA+ valorizam; exportadores beneficiados       |
| Recessão / crise          | Negativo: vacância sobe; cap rate sobe         | Negativo: spread de crédito abre; inadimplência CRI | Muito negativo: inadimplência sobe; subordinação cai | Muito negativo se interno; câmbio alto mitiga para exportadores |

> 📎 **Fonte:** BCB — Relatório de Inflação (2024); BCB — Relatório de Estabilidade Financeira (2024); CEPEA/USP

## 13.2 Calendário Operacional Integrado
| **Periodicidade** | **Atividade**                                                                      | **Output**                                           |
|-------------------|------------------------------------------------------------------------------------|------------------------------------------------------|
| Diário (manhã)    | Variação de preços/P/VP (FII); alertas desmatamento (FIAGRO); inadimplência (FIDC) | Registro de alertas; acionamento de protocolos       |
| Diário (tarde)    | Execução de ordens aprovadas; atualização de modelos afetados por news             | Log de execução; portfólio atualizado                |
| Semanal (4ª)      | Comitê de investimentos: novas teses; revisão de alertas; decisões                 | Ata do comitê; ordens aprovadas                      |
| Mensal (D+5–15)   | Fechamento; cálculo de PL/cota; distribuição de rendimentos; informe CVM           | Informe mensal CVM; relatório de gestão aos cotistas |
| Trimestral        | Revisão estratégica; carta trimestral; revisão dos modelos de valuation            | Carta trimestral; modelos atualizados                |
| Semestral         | Laudos de avaliação (FII/FIAGRO tijolo); revisão de rating (FIDC); AGO             | Laudos; relatório de rating; ata de AGO              |
| Anual             | Demonstrações financeiras auditadas; revisão da política de risco; planejamento    | Demonstrações auditadas; política de risco revisada  |

> 📎 **Fonte:** CVM — Resolução 175/2022 (prazos de reporte); ANBIMA — Código ART 2023 (rotinas de gestão)

# Apêndice A: Fontes e Referências Consolidadas

## A.1 Legislação e Regulação
| **Norma**                    | **Ementa Resumida**                                                     | **Acesso**                                       |
|------------------------------|-------------------------------------------------------------------------|--------------------------------------------------|
| Resolução CVM 175/2022       | Marco dos fundos de investimento; norma-base + anexos por tipo de fundo | cvm.gov.br/legislacao/resolucoes                 |
| Resolução CVM 160/2022       | Ofertas públicas de distribuição de valores mobiliários                 | cvm.gov.br/legislacao/resolucoes                 |
| Resolução CVM 59/2022        | Divulgação de informações ESG por emissores e fundos                    | cvm.gov.br/legislacao/resolucoes                 |
| Resolução CVM 30/2021        | Relatórios e divulgação de informações periódicas de FIIs               | cvm.gov.br/legislacao/resolucoes                 |
| Lei 8.668/1993               | Criação dos FIIs; propriedade fiduciária; vedações ao administrador     | planalto.gov.br                                  |
| Lei 11.196/2005 (Lei do Bem) | Benefícios fiscais para FIIs; isenção IR PF (art. 3º)                   | planalto.gov.br                                  |
| Lei 14.130/2021              | Criação do FIAGRO; equiparação fiscal ao FII                            | planalto.gov.br                                  |
| Lei 11.076/2004              | Cria CRA, CDA, WA, CDCA e LCA                                           | planalto.gov.br                                  |
| Lei 8.929/1994               | Institui a Cédula de Produto Rural (CPR)                                | planalto.gov.br                                  |
| Resolução BCB 29/2020        | Requisitos para custodiante de FIDC                                     | bcb.gov.br/estabilidadefinanceira/exibenormativo |
| Resolução BCB 196/2022       | Regulação prudencial de IFs que atuam em fundos                         | bcb.gov.br/estabilidadefinanceira/exibenormativo |

## A.2 Documentos ANBIMA e Autorregulação
| **Documento**                           | **Conteúdo**                                                     | **Acesso**                                       |
|-----------------------------------------|------------------------------------------------------------------|--------------------------------------------------|
| Código ART (2023)                       | Administração de Recursos de Terceiros — boas práticas de gestão | anbima.com.br/regulacao/codigos-e-guias          |
| Manual de Marcação a Mercado (2024)     | Metodologia de apreçamento de ativos de fundos                   | anbima.com.br/informacoes/manuais                |
| Código de Ofertas Públicas (2023)       | Boas práticas em IPOs e follow-ons de fundos                     | anbima.com.br/regulacao/codigos-e-guias          |
| Classificação de Fundos ANBIMA (2024)   | Taxonomia e classificação de fundos de investimento              | anbima.com.br/informacoes/fundos-de-investimento |
| Boletim de Fundos Estruturados (mensal) | Dados de PL, emissões e evolução de FIDCs, FIIs e FIAGROs        | anbima.com.br/informacoes/fundos-estruturados    |
| Guia de Melhores Práticas de RI (2023)  | Comunicação com cotistas; relatórios de gestão                   | anbima.com.br/regulacao/guias                    |

## A.3 Fontes de Dados de Mercado
| **Fonte**            | **Dados Disponíveis**                                          | **URL / Acesso**                           |
|----------------------|----------------------------------------------------------------|--------------------------------------------|
| CVM — Dados Abertos  | Informes mensais, demonstrações, PL, carteiras de fundos       | dados.cvm.gov.br                           |
| B3 — Portal de Dados | Preços, volumes, IFIX, ex-dividendos, ficha dos fundos         | b3.com.br/pt_br/market-data-e-indices      |
| Banco Central — SCR  | Sistema de Informações de Crédito; histórico de endividamento  | bcb.gov.br/estabilidadefinanceira/scr      |
| IBGE — SIDRA         | IPCA, PIB, construção civil, censo agropecuário                | sidra.ibge.gov.br                          |
| FGV-IBRE             | IGP-M, IPC, custo da construção, Monitor do PIB                | portalibre.fgv.br                          |
| CEPEA/USP            | Preços de commodities agropecuárias (soja, milho, boi, etc.)   | cepea.esalq.usp.br                         |
| INPE — TerraBrasilis | Monitoramento de desmatamento (PRODES, Deter); API disponível  | terrabrasilis.inpe.br                      |
| MAPA — Portal Zarc   | Zoneamento Agrícola de Risco Climático por município e cultura | zarc.mapa.gov.br                           |
| SICAR                | Cadastro Ambiental Rural; status de imóveis                    | car.gov.br                                 |
| IBAMA                | Embargos ambientais; SINAFLOR; autos de infração               | ibama.gov.br                               |
| Quantum Axis         | Dados consolidados de fundos, séries históricas, screener      | quantum.com.br (pago)                      |
| SiiLA Brasil         | Vacância, absorção, cap rates por segmento e cidade            | siila.com.br (pago)                        |
| CBRE Research        | Relatórios de mercado imobiliário; cap rate surveys            | cbre.com/pt-br (gratuito — versão pública) |
| JLL Brasil Research  | Relatórios de mercado imobiliário por segmento                 | jll.com.br (gratuito — versão pública)     |

## A.4 Publicações Técnicas e Metodologias de Rating
| **Publicação**                                   | **Emissor**             | **Relevância**                                                            |
|--------------------------------------------------|-------------------------|---------------------------------------------------------------------------|
| FII Rating Criteria Brasil (2024)                | Fitch Ratings           | Metodologia de análise de FIIs e CRIs para rating                         |
| FIDC Rating Criteria Brasil (2024)               | Fitch Ratings           | Critérios de estrutura, subordinação e análise de carteira                |
| CRA Rating Methodology (2023)                    | Moody's Local BR        | Metodologia de análise de CRAs e FIAGRO-Crédito                           |
| Structured Finance Surveillance (2024)           | S&P Global Ratings      | Monitoramento contínuo de FIDCs e FIIs de papel                           |
| Relatório de Estabilidade Financeira (semestral) | Banco Central do Brasil | Risco sistêmico; inadimplência; setor financeiro                          |
| Fixed Income Analysis (CFA Program, 2024)        | CFA Institute           | Duration, convexidade, análise de crédito — referência técnica            |
| ABNT NBR 14653                                   | ABNT                    | Metodologia de avaliação de bens imóveis (obrigatória para laudos de FII) |
| Manual de Georreferenciamento                    | Incra                   | Georreferenciamento e certificação de imóveis rurais                      |

*Este material tem finalidade exclusivamente educacional e informativa.*

*Não constitui aconselhamento de investimento, jurídico ou regulatório.*

*Legislação e práticas de mercado até 2025. Verifique sempre a versão mais recente das normas e fontes citadas.*
