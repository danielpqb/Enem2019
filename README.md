# EstudosEnem2019
Este repositório é um projeto voltado em analisar os dados dos participantes do Enem 2019 a fim de entender o cenário da educação brasileira.

Para esse projeto baixei o arquivo 'MicrodadosEnem2019.csv' no site do Inep, que infelizmente excluiu os links para download, e agora oferece dados reduzidos apenas para o ano de 2020 em diante.

De início o arquivo possuía cerca de 3 Gb de tamanho com mais de 5 milhões de linhas e 136 colunas. Meu primeiro desafio foi conseguir enxugar os dados que eu não iria utilizar.

# 'Reduzir.ipynb':
Tentei de diversas formas abrir esse arquivo gigantesco em alguns programas como: Excel, Access e MySQL Workbench. Mas totalmente sem sucesso, o arquivo era grande demais para a memória dos programas.
O único programa que consegui rodar foi no Microsoft Power BI, mas com muita lentidão para manipular os dados.
A melhor solução que encontrei foi tratar os dados em Python usando o Pandas. E melhor ainda, no JupyterNotebook para ter melhor visualização ao executar o código em etapas.
Utilizei bastante memória RAM para isso, mas o resultado foi supreendente. Tanto a velocidade de execução quanto a capacidade de desenvolver e refazer etapas foi excepcional.

# 'SubstituirIndicadoresPorTexto.ipynb':
Após reduzir o tamanho do arquivo de quase 3 Gb para 877 Mb, o arquivo ainda era muito difícil de entender pois os valores das células estavam codificados. Para isso precisei de um jeito de ler o dicionário fornecido pelo Inep e substituir os números por textos.
Resolvi da seguinte forma:
Abri o dicionário no Excel e escrevi alguns códigos em VBA para ler e separar os dados. Dessa forma o script já me entregava uma string com o comando que eu precisaria usar em Python.
O resultado final foi um arquivo de 1.87Gb muito mais legível, e que excluia os dados que não eram importantes para o estudo.

# Estudo dos dados
Finalmente consegui abrir o arquivo no Power BI com os dados já tratados, o que já me levou direto a fazer os estudos que eu queria.
Primeiramente separei um grupo específico de estudantes que chamei de 'Compromissados'. Os compromissados são estudantes que:
1) Estavam presentes em todas as provas.
2) Não foram eliminados por qualquer motivo.
3) Não eram 'treineiros'. obs.: Para o Inep treineiro é aquele aluno que só foi fazer a prova para ter a experiência de fazer.
Ou seja, o 'Compromissados' são aqueles que se esforçaram em estar presentes em todas as provas e deram o seu melhor sem trapacear.

<img src="https://cdn.discordapp.com/attachments/387391441397350411/996985890050146435/download.png" />

A minha principal observação nos dados foi a seguinte:
As diferenças de idade, sexo, cor e região são insignificantes na nota final do aluno. Mas quando olhamos para a diferença dos compromissados para a média geral, já é possível ver uma diferença discrepante.
