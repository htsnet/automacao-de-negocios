# automacao-de-negocios
Projeto de Automação de Negócios com Inteligência Artificial

Este projeto tem como objetivo a geração de um modelo que permita a automação de decisões de negócios.

Baseia-se em uma tabela histórica de simulações de aplicações, com dados fornecidos pela B3 de São Paulo.

As operações são de derivativos de contrato de dólar futuro.

Descrição dos campos:

- CodOp = Código interno da operação (sem significado)
- Hora Entrada = Hora da compra
- Hora Saida = Hora da venda
- Duração = Intervalo de tempo entre saída e entrada
- Data = Data da operação
- Pentrada = Preço do papel no momento da compra
- Psaida = Preço do papel no momento da venda
- Ganhos = Diferença entre compra e venda, se >= 0
- Perdas = Diferença entre compra e venda, se < 0
- Resultado = Resultado da operação (1 = ganho, 2 = perda) <-- target
- Ganho Trade =
- K entra =
- K Saida =
- Item 1 = classificador número 1
- Item 2 = classificador número 2
- ...
- Item 77 = classificador número 77

Os campos da operação são dados históricos obtidos diretamento através da B3. Já os classificadores (Item 1 até Item 77, por exemplo) são calculados pelos proprietários do projeto, de acordo com a análise técnica desenvolvida por estes.

Obs. Todos os classificadores são numéricos e sem valores nulos.

A diferença entre os 2 arquivos disponibilizados é na estrutura dos campos. A quantidade de linhas é a mesma. Ambos podem ser utilizados no notebook, bastando apenas trocar o nome para o uoload.

A ideia do projeto tem como seus proprietário Farley Souza e Agnaldo Clozer Pinheiro. A análise do problema e o desenvolvimento do modelo é de Hamilton Tenório da Silva.
