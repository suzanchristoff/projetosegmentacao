# PROJETO SEGMENTAÇÃO DE CLIENTES

- **FICHA TÉCNICA**
    - **OBJETIVO**
        
        O presente projeto teve por objetivo responder às questões de negócio levantadas pela empresa fictícia EL MERCADO, as quais incluíam:
        
        - Entender as mudanças nas preferências dos consumidores;
        - Superar as dificuldades de fidelização;
        - Manter e aumentar as receitas de vendas
        - Desenvolver estratégias de marketing direcionadas para a retenção de clientes
    - **EQUIPE**
        
        Trabalho realizado individualmente por Suzan Christoff
        
    - **FERRAMENTAS E TECNOLOGIAS**
        
        As principais ferramentas e tecnologias utilizadas neste projeto foram:
        
        Spreadsheets e  Looker Studio
        
    - **PROCESSAMENTO E ANÁLISE**
        
        Para dar início a análise, procurou-se entender onde os dados estavam disponíveis, de que tipo eram e como estavam armazenados, para então, saber quais dados seriam necessários para responder às questões levantadas. Em seguida, foi dado início ao processo geral de análise que consistiu nas seguintes etapas:
        
    - **1 Processamento e preparação da base de dados**
        
        1 .1  Importação dos dados: feita através da função *importrange* . No caso desse projeto os dados estavam divididos em 3 tabelas distintas;
        
        1.2  Identificação dos dados nulos: feita através da função COUNTBLANK ;
        
        1.3  Tratamento dos dados nulos: após a identificação dos dados nulos, no caso dos 24 clientes que não tinham a informação de salário, optou-se por atribuir a eles o valor da mediana dos salários dos demais clientes. Já em relação a tabela que continha o registro de todas as transações realizadas pelos clientes, foram identificadas 7 transações às quais não havia atribuição de ID de cliente, e que por se tratar de um número não significativo, foram desconsideradas da análise;
        
        1.4 Identificação e tratamento dos dados duplicados: foram identificados 9 clientes com ID’S duplicadas na tabela resumo de compras. Por se tratar de uma tabela resumida por ID de cliente, entende-se que esses dados não poderiam estar duplicados, portanto, foram também, retirados da análise;
        
        1.5  Identificação e gestão dos dados fora do escopo: foram identificados outliers nos dados relacionados a idade dos clientes e salários dos clientes, entretanto, optou-se por mantê-los e agrupá-los em suas respectivas faixas de valores;
        
        1.6  União das tabelas: foi feita através das funções PROCV E QUERY.
        
        1.7  Criação das seguintes variáveis: “tem_filhos”, “total_compras”, “idade”, “faixa_etária”, “faixa salarial”, “recency”, “frequency”, “monetary”, “segmentos”, “score_R”, “score_F”, “score_M”, “media_score_FM”
        
    - **2 Processo da análise exploratória dos dados**
        
        2.1 Agrupamento dos dados de acordo com as variáveis categóricas
        
        2.2  Visualização das variáveis através de gráficos simples
        
        2.3 Cálculo das variáveis RFM
        
        2.4 Cálculo de medidas descritivas como média e mediana
        
        2.5 Cálculo dos quintis
        
    - **Efetiva aplicação da técnica de segmentação RFM**
        
        A técnica de segmentação RFM consistiu em calcular há quantos dias foi a última compra de cada cliente (Recency), o número de vezes que realizou compras (Frequency) e o valor monetário total investido nas compras (Monetary). E em seguida fez-se a divisão desses clientes em 5 grupos por meio do cálculo de quintis, aos quais foram atribuídas notas de 1 a 5 para que então finalmente, pudesse ser aplicada a segmentação, com base nas notas recebidas por cada cliente.
        
    - **RESUMO ATRAVÉS DE DASHBOARD**
        
        As informações obtidas através da análise, foram apresentadas por meio de dashboard criado através do LOOKER STUDIO, onde foi possível visualizar de forma geral:
        
        - A receita total gerada no período analisado,
        - O total de transações ,
        - O número total de clientes,
        
        - O ticket médio de cada transação,
        
        - A participação de cada segmento no faturamento,
        - Os produtos consumidos para cada segmento,
        - O números de novos clientes registrados a cada mês
        
        Observação: uma segunda página foi acrescentada ao dashboard para que se pudesse explorar ainda mais o perfil socioeconômico de cada segmento
        
    - **TÉCNICAS DE ANÁLISES APLICADAS**
        
        Para que o resultados desejados fossem obtidos, optou-se por usar a **Técnica de Segmentação RFM** , calculada conforme descrito anteriormente.
        
    - **RESULTADOS, CONCLUSÕES E RECOMENDAÇÕES**
        
        Através da análise realizada, os seguintes resultados foram obtidos:
        
        - O primeiro maior segmento de clientes identificado, de acordo com sua representatividade no faturamento da empresa, foi o de clientes campeões (28%), seguido dos clientes em risco (26%) e clientes fiéis (21%), os quais representam, portanto, mais de 70% do total da receita.
        - Foi observado um padrão de consumo em todos os segmentos, onde os produtos mais consumidos são o vinho e a carne
        - O número de novos clientes mensais não varia muito, ficando em torno da média de 93 clientes
        - Observou-se  que nos últimos 6 meses analisados, houve um decréscimo no número de transações.
        - Verificou-se que o ticket médio por transação dos clientes que não tem filhos é 2 vezes maior do que ticket dos clientes com filhos.
        - Apenas 11% dos clientes têm ensino secundário, os demais têm ensino superior ou pós graduação.
        - A maior parte dos clientes tem idade entre 40 e 69 anos
        - O canal que gera mais vendas é o canal físico , representando 58% das vendas.
        
        Com base nos resultados mostrados, focamos nossas sugestões nos grupos de clientes com maior representatividade. Assim sendo, sugerimos:
        
        - Em relação aos clientes campeões e fiéis , acreditamos que é um segmento que pode ser recompensado através de prêmios, descontos ou outras experiências que os façam se sentirem reconhecidos e  assim, possam fazer a indicação de novos clientes. Importante também é entender qual é a motivação que leva esse segmento a ser tão fiel à marca da empresa , afim de tornar a sua participação ainda maior.
        - Já em relação aos clientes em risco acreditamos ser importante melhorar o pós venda e que sejam descobertas as razões de não estarem mais comprando da empresa. Uma boa opção também é oferecer novos produtos ou similares aos que consumiam, para que novamente despertem o interesse pela marca da empresa.
