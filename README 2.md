# Dashboard Looker Studio: O Ciclo de Vida Empresarial no Paraná

Projeto acadêmico de Análise de Dados desenvolvido pela **FAE** em parceria com o **SEBRAE**, com foco na análise estratégica do ecossistema empresarial paranaense. Por meio da inteligência de dados, o dashboard avalia o ciclo de vida das empresas para gerar inteligência de mercado e apoiar decisões de negócios em nível estadual.

**[Acesse o dashboard interativo no Looker Studio](https://datastudio.google.com/reporting/afbe08f4-6960-420f-b430-67a903edced7)**

---

## Metodologia e escopo

A análise mapeia **1.838.142 empresas ativas** distribuídas pelos **399 municípios do Paraná**, com projeção de cenários até 2025. O projeto é dividido em quatro fases do ecossistema empresarial:

1. O Nascimento
2. A Sobrevivência
3. A Estabilidade
4. A Oportunidade

- **Fonte de dados:** base primária fornecida pelo SEBRAE.
- **Tratamento inicial:** limpeza, padronização e higienização estrutural no Microsoft Excel.

### Regras de negócio e indicadores exclusivos

Para transformar dados brutos em ferramentas de decisão, a equipe desenvolveu métricas próprias:

- **Score de Resiliência:** indicador composto (0 a 100) que mede a preparação de um município para sustentar empresas no longo prazo. Pesos da fórmula:

  | Componente | Peso |
  |---|---|
  | Baixa inaptidão | 30% |
  | PIB per capita | 25% |
  | Taxa de maturidade | 25% |
  | IDH-M | 20% |

- **Quadrante Mágico de Investimento:** inspirado em matrizes de consultoria, cruza o **IPC Total** (potencial de consumo) com o **Saldo CAGED** (saldo de contratações) e classifica as cidades em quatro zonas de mercado: **Estrela** (alto consumo e geração de empregos), **Aposta**, **Madura** e **Risco**.

---

## Principais insights

- **Rotas de consumo de alta renda:** Curitiba domina o potencial de consumo, impulsionada pelas classes B1 e A. O eixo Curitiba–Londrina–Maringá se mostra a zona ideal para investimentos com foco em alto volume e renda urbana.
- **Liderança em resiliência:** Araucária lidera o estado, com **74,13 pontos** no Score de Resiliência, pela combinação de baixo encerramento de empresas e alto PIB per capita.
- **Oportunidades fora do radar:** Indianópolis surge como a "cidade surpresa". Com menos de 50 mil habitantes, atinge **71,84 pontos** graças ao excelente PIB, o que a torna uma aposta rentável e menos saturada.

---

## Detalhes técnicos e modelagem no Looker Studio

Para viabilizar a análise sem recorrer a bancos de dados relacionais externos, o projeto explorou recursos avançados da ferramenta:

- **Combinação de dados (data blending):** mesclagens criadas diretamente no Looker Studio (ex.: "PIB vs Inaptas" e "Ativas x Inaptas"), cruzando indicadores macroeconômicos municipais com os registros de CNPJs.
- **Governança e lógica de filtros:** sistema rigoroso de regras para garantir a precisão das visualizações, com destaque para o "Filtro Empresas Inaptas" (5 cláusulas lógicas combinadas) e parametrizações de escopo (restrição regional `UF = PR` e segmentação por porte: MEI, ME, EPP, GOV, SFL).
- **Tratamento cartográfico e de outliers:** regras de inclusão e exclusão para municípios que distorciam a escala dos dados (ex.: isolamento ou exclusão de Mirador, Curitiba, Araucária e Indianópolis em visualizações comparativas específicas).

---

## Tecnologias

`Looker Studio` · `Microsoft Excel` · `Data Blending` · `Indicadores compostos`

---

## Visualização do dashboard

### Capa
<img src="images/01-capa.jpeg" alt="Capa do dashboard Insight Project for Business" width="700" />

### 1. O Nascimento
<img src="images/02-nascimento-empresas-ativas.jpeg" alt="O Nascimento: empresas ativas por porte e por município" width="700" />

<img src="images/03-nascimento-tempo-de-abertura.jpeg" alt="O Nascimento: tempo médio de abertura de empresas" width="700" />

### 2. A Sobrevivência
<img src="images/04-sobrevivencia-mapa-de-calor.jpeg" alt="A Sobrevivência: mapa de calor da inaptidão por região" width="700" />

<img src="images/05-sobrevivencia-risco-x-riqueza.jpeg" alt="A Sobrevivência: matriz risco x riqueza e cidades em alerta" width="700" />

### 3. A Estabilidade
<img src="images/06-estabilidade-maturidade.jpeg" alt="A Estabilidade: empresas ativas e maturidade de mercado" width="700" />

<img src="images/07-estabilidade-potencial-de-consumo.jpeg" alt="A Estabilidade: potencial de consumo por cidade e classe social" width="700" />

### 4. A Oportunidade
<img src="images/08-oportunidade-quadrante-magico.jpeg" alt="A Oportunidade: Quadrante Mágico de Investimento" width="700" />

<img src="images/09-oportunidade-score-de-resiliencia.jpeg" alt="A Oportunidade: Score de Resiliência por município" width="700" />

---

## Equipe FAE

Projeto desenvolvido em colaboração por:

- Isabella Soberay
- Luana Barrios
- Mariane Maestri
- Suzana Faucz
