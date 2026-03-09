# Score de Crédito dos Clientes

Você foi contratado por um banco para conseguir definir o score de crédito dos clientes. Você precisa analisar todos os clientes do banco e, com base nessa análise, criar um modelo que consiga ler as informações do cliente e dizer automaticamente o score de crédito dele: Ruim, Ok, Bom.

---

## Base de Dados

A base de dados possui 100.000 linhas e 25 colunas,, sendo elas:

| id_cliente | mes | idade | profissao | salario_anual | num_contas | num_cartoes | juros_emprestimos | num_emprestimos | dias_atraso | num_pagamentos_atrasados | num_verificacoes_credito | mix_credito | investimento_mensal | divida_total | taxa_uso_credito | idade_historico_credito | comportamento_pagamento | saldo_final_mes | score_credito | emprestimo_carro | emprestimo_casa | emprestimo_pessoal | emprestimo_credito | emprestimo_estudantil |

## Visualizar a base de dados

Visualização da base de dados para compreensão das informações relevantes para a análise e se há a necessidade de tratar algum campo por causa do conflito do tipo de dado.

<img width="1117" height="360" alt="image (3)" src="https://github.com/user-attachments/assets/3e79697e-f6be-4a01-842a-9229f8762677" />

<img width="1108" height="342" alt="image (4)" src="https://github.com/user-attachments/assets/49d8033f-9a41-49ec-9cae-947e978f496f" />

<img width="772" height="336" alt="image (5)" src="https://github.com/user-attachments/assets/7b2f56a3-a414-499a-8e70-07c4f4916941" />
[Tabela completa exibindo as colunas e o preenchimento dos dados dos clientes.]

## Tratamento de dados

Observação dos tipos de dados das colunas para saber quais tipos de dados precisarão ser tratados.

<img width="358" height="393" alt="image (6)" src="https://github.com/user-attachments/assets/dc5b7f97-0dff-4ca1-8080-20fe9b637630" />

[Base de dados com colunas e tipos de dados.]

- Removida a coluna id_cliente
<img width="1114" height="325" alt="image (7)" src="https://github.com/user-attachments/assets/6fb84987-456d-4e34-8043-314eac95c0b6" />

[Base de dados após a exclusão da coluna id_cliente.]

- Tratamento de dados do tipo object realizado nas colunas profissão, mix_credito e comportamento_pagamento.

<img width="77" height="340" alt="image (8)" src="https://github.com/user-attachments/assets/05326b6e-5b16-4767-97b2-137ccf882b41" />
<img width="69" height="335" alt="image (9)" src="https://github.com/user-attachments/assets/422c705e-b3fe-45be-833c-c559f2b5edcd" />
<img width="191" height="351" alt="image (10)" src="https://github.com/user-attachments/assets/920d5f6a-5e59-4840-900a-d490dc97aed3" />
<img width="167" height="357" alt="image (11)" src="https://github.com/user-attachments/assets/5d3448af-3b8c-4fe4-a1ed-1215b7d1cc16" />

## Treinamento dos modelos

Foram utilizados 30% dos dados para teste e 70% dos dados para treino.

O primeiro modelo utilizado para treinamento foi o RandomForest (Árvore de Decisão) e o segundo modelo foi o KNN. 

Com isso, após o treinamento, foi possível obter a porcentagem da precisão retornada por ambos os modelos.

<img width="318" height="90" alt="image (12)" src="https://github.com/user-attachments/assets/6bc055bc-a7cc-42fc-bb3f-74950db3b772" />

[Resultado da acurácia dos modelos]

## Previsão

Após observar o modelo de Árvore de Decisão como sendo o melhor para prosseguir, foi realizado o teste a partir do treinamento da entrada dos 30% dos dados reservados para teste.

Após tratamento dos dados reservados para teste e aplicação sob o modelo escolhido foi possível prever o resultado com base nas novas entradas como indicado nas imagens a seguir.

<img width="1088" height="126" alt="image (13)" src="https://github.com/user-attachments/assets/1fba5728-d010-4e9d-866f-c91c49930eac" />

[Exibição da previsão de Score de Crédito a partir do modelo de Árvore de Decisão]

Com base nos dados inseridos, o modelo retornou como resultado “Poor”, “Poor” e “Standard”.







