# Business Intelligence - ETL e Carga Incremental com Pentaho Data Integration e Pentaho Server

Projeto Desenvolvido no Pentaho Data Integration de ETL e carga. Onde foi criado stages, dimensões, fato, data warehouse e um Job principal para executar a carga incremental via Pentaho Server.

1) O projeto se inicia através da organização primeiramente da Stage Area.

Stage das Tabelas Dimensões:

- Stage Clientes
- Stage Detalhe dos Pedidos
- Stage Pedidos
- Stage Produtos

Stage da Tabela Fato:

Stage Fato Pedidos

2) Envio dos dados semi tratados das stages para o Banco de dados nesse exemplo chamado de 'stg' no HeidiSQL.

3) A partir dos stages é criado o Data Warehouse, com chaves específicas criadas para cada tabela Dimensão e Fato. 

4) Carregamento das tabelas Dimensão e Fato no DW e criação de uma nova Dimensão Calendário. 

5) Lookup das tabelas e criação de tabelas de Log.

6) Criação da carga incremental nesse exemplo realizado com Merge diff, atualizando somente os dados alterados e mantendo o restante dos dados iguais. 

7) Criação de um Job principal para executar todas as tranformações e cargas de forma otimizada.

8) Conexão com Pentaho Server e gerar agendamento da carga incremental. 



Stage Dimensão Cliente

![stg1](https://user-images.githubusercontent.com/109915092/213242116-ac9ae94e-08bf-4786-978a-6b39a6a7abf0.png)

Stage Dimensão Detalhe do Pedidos

![stg2](https://user-images.githubusercontent.com/109915092/213245972-b1ae474b-5792-4adf-9bba-8b6292ee500f.png)

Stage Dimensão Pedidos

![stg3](https://user-images.githubusercontent.com/109915092/213252561-7948b9af-25e6-499d-b374-637a1cff7f58.png)




