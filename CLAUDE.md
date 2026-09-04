# Brain003 — Contexto do Projeto

## O que é a Brain003

Brain003 (grafia canônica; nunca "Brain3" ou "Brain 003" em texto novo — ver
`design.md`) é o laboratório de inteligência de dados e comportamento do
**Grupo Arka**. Conecta o ecossistema de parceiros do grupo, transformando
dados de fidelização, consumo e mídia em decisões baseadas em evidência.

**Conceito oficial** (fonte: `BRAIN3 Conceito e Posicionamento.pdf`):
> Brain3 é uma empresa de inteligência de dados. Um ambiente onde
> comportamentos de consumo, fidelização e mídia são captados pelas empresas
> do Grupo Arka e outros players do ecossistema, são coletados, analisados e
> transformados em decisões baseadas em evidência.

Modelo de operação: **Coleta/Normalização → Análise → Ação**.

## O desafio de mercado que a Brain endereça

- Dados fragmentados entre mídia, vendas, ERPs, CRM e fidelidade, sem cruzamento.
- Privacidade e compliance: LGPD e fim dos cookies de terceiros dificultam
  cruzar dados entre marcas e parceiros.
- Ferramentas genéricas de analytics não enxergam o contexto/peculiaridade
  de cada operação.
- Insight sem ação: relatórios geram diagnóstico, mas a execução fica
  desconectada.

A resposta é posicionar a Brain como um **Data Clean Room**: ambiente seguro
e neutro onde dados de diferentes fontes se cruzam sem que nenhuma parte
acesse o dado bruto da outra — só resultados agregados, com compliance
nativo à LGPD mesmo no cenário pós-cookies.

## Estrutura do grupo

- **Grupo Arka** — holding. A Brain003 opera como camada de inteligência
  entre as empresas do grupo e o ecossistema de parceiros externos.
- **Minu** — empresa irmã, opera clubes de recompensa/fidelidade para
  clientes corporativos (bancos, varejo, alianças), monetizando via % sobre
  valor de recompensa ou taxa/quebra em programas bancários. Fonte principal
  de dados transacionais de fidelização (acúmulo, resgate, comportamento de
  pontos) que a Brain analisa. Relação mais antiga e relevante: Banco do
  Brasil (~16 anos), Recompensas Digitais ~R$31M/ano (60% da receita da
  Minu). Prioridade estratégica atual: UAU Caixa, em queda desde o Pix
  (~13M → ~4M pontos/mês).
- **Core** — também sob a Arka, atua em conjunto com a Minu: dados de
  performance de mídia e campanhas digitais; marketing/comunicação de
  campanha ficam com a Core. Empresa parceira independente, não subsidiária
  da Minu.
- **Consórcio Sirius** — Minu lidera + GoPoints + Easy Live. A Caixa é
  cliente do consórcio, não membro.
- Parceiros/marcas cujos dados alimentam o ecossistema (ver slide "Como" da
  apresentação): TIM, Banco do Brasil, BV, Banco Mercantil, BB Seguros,
  Bradesco, Outback, Oscar, O Boticário, Torra, Partage Malls, Pefisa,
  PicPay, Caedu, Caixa, Cashin, CiClic, Credsystem, Primeira Mesa, Intelbras,
  Ingresso.com, Inner AI, McDonald's, Natura, Aby's, cinemas Arcoplex, C&A,
  Chillibeans, Madero, Nebula Cinemas, 99, Nintendo, Itaú, CNA Go, Claro,
  Caveon, Carrefour, Casas Bahia, entre outros.

## Meta e prioridades de negócio (ano 1)

- Meta verbalizada no kickoff/onboarding: **dobrar (2x)** o faturamento
  conjunto Minu+Core, buscando revenue share — não "triplicar" (checar se
  há meta mais nova antes de citar um múltiplo diferente).
- Prioridade imediata de receita: projeto **Caixa Cartões** (dashboard
  executivo de indicadores financeiros), em 3 fases — 60 dias (dashboard
  inicial) → 90 dias (integração via API) → camada de inteligência com LLM.
- Varejo é o pilar de maior crescimento ("oceano azul" por falta de
  ferramenta avançada no setor).
- Mudança de modelo de negócio em curso: de "venda de token" para "cobrança
  pela inteligência entregue" — a Brain como gatekeeper/orquestrador, mesmo
  quando o cliente usa seus próprios modelos de linguagem.
- Detalhe completo de dores e oportunidades por área (negócios, dados,
  operações, relacionamento BB): ver `minu-discovery.md`.

## Módulos (5 módulos ativos)

1. **Painel de 360°** — jornada completa do cliente, detecção de mudanças
   de comportamento, hipersegmentação.
2. **Painel de Produtos** — performance de SKUs, ticket médio, market
   basket, elasticidade de preço, painel da concorrência.
3. **Brain Score** — score de crédito alternativo baseado em dados
   transacionais e histórico de fidelização.
4. **Campaign Analytics** — atribuição multi-touch, ROI de mídia,
   otimização de budget/canal, hipersegmentação de audiências.
5. **Converse com seus dados** — consulta em linguagem natural (modelo
   LLM) + Consultoria Estratégica (modelos preditivos sob medida).

Frase-síntese oficial: *"É o que acontece quando os 5 módulos operam sobre
a mesma base de dados, dentro do mesmo Clean Room, ao mesmo tempo."*

## Features (montadas a partir dos módulos)

As features são o que o cliente compra/usa — cada uma combina um ou mais
módulos acima por trás. É a camada de produto exposta no site (Home →
Features), não uma lista separada de capacidades.

1. **Paid Media Optimization** — Score de campanha cruzado com CRM e mídia
   paga do cliente, dentro do Clean Room; indicadores em tempo real.
2. **CDP** — hipersegmentação e enriquecimento de audiência via ecossistema
   Arka, alimentando campanha e treinando IA sem recomeçar do zero por canal.
3. **Analytics Agents** — agentes de IA que definem audiência, criativo,
   canal e verba a partir de objetivo/perfil, e reajustam sozinhos conforme
   o resultado chega (ROAS previsto, não só medido depois).
4. **AI Synthetic Brain** — simulação de produto, preço e persona com IA
   treinada em comportamento real de consumo, antes de ir a mercado.
5. **Market Intelligence** — inteligência de mercado via crowdsourcing de
   pesquisa (rede de campo do Bora), cruzada com dado transacional do
   ecossistema Arka.

*(Em aberto: qual módulo alimenta qual feature ainda não está mapeado
1:1 — só sinalizando a lacuna em vez de inventar a correspondência.)*

### Brain Network (efeito de rede entre marcas)
Além dos módulos/features individuais, a Brain gera valor cruzando dados
entre marcas do ecossistema sem expor dado bruto entre elas:
- **Audiências compartilhadas** — ativar cliente fiel de uma marca em outra
  marca por similaridade comportamental, sem identificação individual exposta.
- **Mídia cruzada (co-op media)** — marcas dividem custo/inventário de
  mídia para alcançar públicos sobrepostos, medido pelo Paid Media Optimization.
- **Crédito coletivo** — Brain Score calculado sobre o comportamento
  combinado da coalizão, sinal mais forte que o de qualquer marca isolada.

## Identidade visual

O sistema de design (cores, tipografia, componentes, logomark, regras de
Do's/Don'ts) está documentado em [`design.md`](design.md), seguindo o
formato aberto DESIGN.md (stitch.withgoogle.com/docs/design-md/specification).
Leia-o antes de gerar, editar ou revisar qualquer UI, slide, peça de
papelaria ou post — trate seus tokens e regras de componente como
vinculantes, salvo instrução explícita em contrário do usuário. Referência
humana complementar (brandbook de apresentações): `Brain003-Brandbook.html`.
