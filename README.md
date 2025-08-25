Análise de E-commerce
📌 Contexto
Desenvolvimento de um painel analítico que auxilie a área comercial e de logística a tomar decisões baseadas em dados.
O painel deve mostrar a evolução das vendas, o comportamento dos clientes e a gestão do estoque nos últimos 3 anos.

Objetivos do Painel
O painel deve conter as seguintes visões e KPIs:

Comparativo de vendas (últimos 3 anos)

Valor Liquido por mês, com comparação ano a ano.
Evolução do estoque no período

Qtd Estoque por produto, categoria e total.
Novos clientes por mês

Definição: primeira compra no mês de referência.
Clientes inativos

Definição: última compra há mais de 6 meses.
Vendas acumuladas (YTD)

Exibir por canal e categoria.

Média de itens vendidos (últimos 30 dias)

Média diária de Qtd considerando os últimos 30 dias.

📏 Regras de Negócio Esperadas

Primeira compra = MIN(DataHoraVenda) por ClienteID

Última compra = MAX(DataHoraVenda) por ClienteID

Novos clientes = primeira compra no mês

Inativos = última compra anterior a (data de referência – 180 dias)

Ticket médio 
YTD = soma de ValorLiquido no ano até a data selecionada
🛠 Requisitos Técnicos
Modelagem em estrela (fatos e dimensões separadas)

