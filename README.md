# Mercado de Aberturas de Empresas — Case Analítico 2026

Análise do mercado brasileiro de abertura de empresas com projeção de demanda para 2026, identificação de sazonalidade, concentração regional e estratégia de aquisição de clientes.

---

## Contexto

O mercado de abertura de empresas no Brasil cresceu de forma consistente entre 2018 e 2025, encerrando o último ano com 335 mil aberturas — alta de 16% sobre 2024. Desse total, 96% correspondem a MEI e pequenos negócios, o que define o perfil predominante do público-alvo.

O objetivo deste projeto foi estruturar uma base analítica para orientar as decisões comerciais da empresa em 2026, respondendo a três perguntas centrais:

1. Qual o tamanho do mercado projetado para 2026?
2. Onde e em quais segmentos a demanda se concentra?
3. Como estruturar a estratégia de aquisição com base nesses dados?

---

## Estrutura do Projeto

```
.
├── analise.ipynb               # Notebook principal com toda a análise
├── Dados_Case_2026.xlsx        # Base de dados histórica (2018–2025)
├── grafico_historico.png       # Série histórica mensal
├── grafico_decomposicao.png    # Decomposição da série temporal
├── grafico_projecao.png        # Projeção 2026 com histórico
├── grafico_concentracao.png    # Market share por região
└── grafico_meta.png            # Meta mensal de vendas (20% de market share)
```

---

## Metodologia

### Projeção de mercado

A taxa de crescimento anual foi calculada como a média dos três últimos anos (2023–2025), excluindo os picos atípicos do pós-pandemia. O valor encontrado foi de **11,4%**, aplicado sobre o total de 2025 para estimar **373 mil aberturas em 2026**.

A distribuição mensal foi feita com base no índice sazonal histórico — razão entre a média de cada mês e a média geral — preservando o padrão observado nos dados: julho e agosto como meses de pico, dezembro e janeiro como os mais fracos.

### Decomposição da série temporal

A série foi decomposta em três componentes:

- **Tendência**: crescimento contínuo ao longo dos 8 anos analisados
- **Sazonalidade**: padrão mensal estável e reprodutível
- **Resíduos**: controlados, com exceção do outlier da pandemia em 2020 (índice 0,52)

### Análise de volatilidade

A volatilidade de cidades e segmentos foi medida pelo coeficiente de variação (CV = desvio padrão / média), permitindo comparações justas entre mercados de tamanhos diferentes.

- Cidade mais volátil: **São Paulo** (CV 1,38) — concentra o maior volume absoluto, o que amplifica qualquer oscilação
- Segmento mais volátil: **Psicologia** (CV 1,49) — crescimento explosivo pós-pandemia tornou o padrão histórico inconsistente

### Testes estatísticos

| Teste | Resultado | Interpretação |
|---|---|---|
| ANOVA (volume por região) | F = 174, p = 0,000 | Cada região tem seu próprio ritmo de mercado |
| Qui-quadrado (segmentos por região) | Chi² = 4,21, p = 1,0 | Os mesmos segmentos abrem em proporções iguais em todo o Brasil |

Isso indica que a empresa precisa de **estratégias comerciais distintas por região**, mas pode criar **conteúdo por segmento com alcance nacional**.

---

## Principais Resultados

| Indicador | Valor |
|---|---|
| Mercado projetado 2026 | 373 mil empresas |
| Crescimento sobre 2025 | +11,4% |
| Meta para 20% de market share | 74 mil vendas |
| Média mensal necessária | 6.224 vendas |
| Concentração SP + Grande SP | 35,9% do mercado |

---

## Concentração Regional

São Paulo e Grande SP respondem por 35,9% de todas as aberturas. O grupo "outros" — cidades menores — representa 41% do mercado e é o de maior potencial de expansão, justamente por estar pulverizado e pouco atendido.

---

## Estratégia de Aquisição

Com base nos dados, foram identificadas três frentes complementares:

**Frente digital** — Manutenção da presença online para capturar freelancers e profissionais liberais que buscam ativamente o serviço por Google e redes sociais.

**Representantes presenciais** — Visitas a pequenos comércios como salões e oficinas, segmentos cujo processo de decisão passa por confiança e contato direto.

**Tráfego geolocalizado com parcerias** — Anúncios segmentados em regiões como Carapicuíba e Itapevi, combinados com parcerias em sindicatos e associações locais para ampliar o alcance no mercado pulverizado.

---

## Tecnologias

- Python 3.14
- pandas
- numpy
- matplotlib
- scipy (ANOVA e qui-quadrado)

---

## Como Executar

```bash
# Instalar dependências
pip install pandas numpy matplotlib scipy openpyxl

# Abrir o notebook
jupyter notebook analise.ipynb
```

O arquivo `Dados_Case_2026.xlsx` deve estar no mesmo diretório do notebook.

---

## Autor

Welington Fonseca da Silva
