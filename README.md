# automacao-de-negocios
Projeto de Automação de Negócios com Inteligência Artificial

Este projeto tem como objetivo a geração de um modelo que permita a automação de decisões de negócios no mercado financeiro.

Baseia-se em uma tabela histórica de simulações de operações financeiras realizadas com base em dados obtidos da B3 – a bolsa de valores brasileira.

As operações financeiras se referem à compra e venda do derivativo dólar futuro (DOL). São também conhecidas como operações de “Day Trade” no mercado futuro.

Descrição dos campos:

- CodOp = Código interno da operação (sem significado)
- Hora Entrada = Hora da compra
- Hora Saída = Hora da venda
- Duração = Intervalo de tempo entre entrada e saída do trade
- Data = Data da operação
- Pentrada = Preço do ativo no momento da compra
- Psaida = Preço do ativo no momento da venda
- Ganhos = Diferença de pontos entre compra e venda, se >= 0
- Perdas = Diferença de pontos entre compra e venda, se < 0
- Resultado = Resultado da operação (1 = ganho, 2 = perda) <-- target
- Ganho Trade =
- K entra = sumarização da hora de entrada, em minutos, a partir do início do pregão
- K Saida = sumarização da hora de saida, em minutos, a partir do início do pregão
- Item 1 = classificador número 1
- Item 2 = classificador número 2
- ...
- Item 77 = classificador número 77

Os campos da tabela que envolvem Data, Hora e Preço são dados históricos obtidos diretamente através da B3. Já os classificadores (Item 1 até Item 77, por exemplo) são calculados pelos proprietários do projeto, de acordo com a análise técnica desenvolvida por estes.

Obs. Todos os classificadores são numéricos e sem valores nulos.

A diferença entre os 2 arquivos disponibilizados é na estrutura dos campos. A quantidade de linhas é a mesma. Ambos podem ser utilizados no notebook, bastando apenas trocar o nome para o uoload.

A ideia do projeto tem como seus proprietário Farley Souza e Agnaldo Clozer Pinheiro. A análise do problema e o desenvolvimento do modelo é de Hamilton Tenório da Silva.

________________________________________________________________

Arquivo 1 - Automacao_de_Negocios.ipynb: Geração do modelo
Arquivo 2 - Automacao_de_Negocios_Uso_Modelo.ipynb: Uso do modelo gerado no arquivo 1 (finalized_model.pkl) para predições de novos dados (novos_dados.csv)

O arquivo novos_dados.csv contém o cabeçalho e os registros com apenas os 77 itens a serem considerados pelo modelo

