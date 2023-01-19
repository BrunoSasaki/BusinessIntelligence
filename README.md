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

2) Job das Stages para envio dos dados semi tratados das stages para o Banco de dados nesse exemplo chamado de 'stg' no HeidiSQL.

3) A partir dos stages é criado o Data Warehouse, com chaves específicas criadas para cada tabela Dimensão e Fato carregado a partir de um 2 Job's. 

4) Carregamento das tabelas Dimensão e Fato no DW e criação de uma nova Dimensão Calendário. 

5) Lookup das tabelas e criação de tabelas de Log.

6) Criação da carga incremental nesse exemplo realizado com Merge diff, atualizando somente os dados alterados e mantendo o restante dos dados iguais. 

7) Criação de um Job principal para executar todas as tranformações e cargas de forma otimizada.

8) Conexão com Pentaho Server e gerar agendamento da carga incremental. 




1. Stage Area


Stage Dimensão Cliente

![stg1](https://user-images.githubusercontent.com/109915092/213242116-ac9ae94e-08bf-4786-978a-6b39a6a7abf0.png)

Stage Dimensão Detalhe do Pedidos

![stg2](https://user-images.githubusercontent.com/109915092/213245972-b1ae474b-5792-4adf-9bba-8b6292ee500f.png)

Stage Dimensão Pedidos

![stg3](https://user-images.githubusercontent.com/109915092/213252561-7948b9af-25e6-499d-b374-637a1cff7f58.png)


Stage Dimensão Produtos

![stg4](https://user-images.githubusercontent.com/109915092/213253037-ce48dc17-337a-4d74-b550-7e99555693c8.png)

Stage Fato Pedidos

![stg5](https://user-images.githubusercontent.com/109915092/213253417-cd081ac5-5b1e-4240-97d2-f322d5d959d5.png)


2. Job das Stages carregado no SQL

![Job Stages](https://user-images.githubusercontent.com/109915092/213254997-ab174490-d786-4a31-8800-b31423129c8f.png)

![Heidisql](https://user-images.githubusercontent.com/109915092/213309438-59d960a6-65a0-4595-9031-9a6e57330bab.png)
