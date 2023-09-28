# Análise de Vendas Farmacêuticas
Análise sobre vendas farmacêuticas no mês de Novembro/2021, com descobertas e insights para industrias farmacêuticas e farmácias.

![imagem_trip](https://github.com/wagnermoraesjr/Analise_de_Vendas_Farmaceuticas/blob/main/vista-superior-variedade-de-medicamentos-e-comprimidos.jpg)

## **Objetivo**

Compreender as tendências, padrões e características das vendas farmacêuticas em diferentes regiões e demografias, atráves da Análise Exploratória de Dados (EDA).

Essa análise dos dados deverá permitir conhecermos as tendências de vendas, os produtos mais vendidos, a demografia dos consumidores e se existe alguma correlação entre as variáveis. Serão plotados alguns gráficos para que possamos ter uma visualização melhor dos dados.

Com base nessa análise dos dados iremos identificar insights sobre os hábitos de compra e padrões dos consumidores.

<br>

## **Introdução**

O Dataset utilizado para essa análise será o **[Medicamentos Industrializados - Novembro de 2021](https://dados.gov.br/dados/conjuntos-dados/venda-de-medicamentos-controlados-e-antimicrobianos---medicamentos-industrializados)** disponibilizado pela Agência Nacional de Vigilância Sanitária - ANVISA no portal de dados do Governo Federal.
<br><br>
**Sobre o conjunto de dados:**

Dados Abertos de Venda de Medicamentos Industrializados do Sistema Nacional de Gerenciamento de Produtos Controlados (SNGPC) de Novembro de 2021.
<br><br>
O Sistema Nacional de Gerenciamento de Produtos Controlados (SNGPC), monitora as
movimentações de entrada (compras e transferências) e saída (vendas,transformações, transferências e perdas) de medicamentos sujeitos à escrituração no SNGPC comercializados em farmácias e drogarias privadas do país.
<br><br>
**Observação:** De acordo com a RDC 586/2021, os prazos para a transmissão dos dados de venda de medicamentos sujeitos ao controle especial foram temporariamente suspensos. Embora os estabelecimentos precisem manter seus registros internos, a partir de 5 de outubro de 2021, a transmissão de dados deixou de ser obrigatória. Adicionalmente, para implementar solução tecnológica no sistema, a partir de 23 de dezembro de 2022 o acesso ao sistema foi interrompido de forma geral. Com isso, a transmissão de arquivos com dados de movimentações de medicamentos e insumos sujeitos ao controle especial ficou opcional, entre 05/10/2021 e 22/12/2022, e passou a ser suspensa, a partir de 23/12/2022.
<br><br>
**Dicionário dos Dados:**

**`ANO_VENDA:`** Ano da venda do medicamento.<br>
**`MES_VENDA:`** Mês da venda do medicamento.<br>
**`UF_VENDA:`** Unidade Federativa do endereço da farmácia ou drogaria, cadastrado no banco de dados da Anvisa, representando a UF onde ocorreu a venda.<br>
**`MUNICIPIO_VENDA:`** Município do endereço da farmácia ou drogaria, cadastrado no banco de dados da Anvisa, representando o Município onde ocorreu a venda.<br>
**`PRINCIPIO_ATIVO:`** Nome do princípio ativo do medicamento industrializado, conforme cadastrado no registro do medicamento, no banco de dados da Anvisa. Quando um medicamento tem mais de um princípio ativo, cada um deles é separado pelo caractere “+”. Ex.: “PRINCÍPIO ATIVO 1 + PRINCÍPIO ATIVO 2”.<br>
**`DESCRICAO_APRESENTACAO:`** Uma apresentação de medicamento representa o modo como um medicamento é apresentado na embalagem. Exemplo: Medicamento X, pode ter duas apresentações diferentes:

*   **Apresentação 1:** Uma caixa com 1 blister de alumínio com 20 comprimidos, cada comprimido com 5 mg de princípio ativo. Nesse caso, a descrição da apresentação seria: “5 MG COM CT BL AL X 20”.
*   **Apresentação 2:** Uma caixa com 1 frasco de vidro com 50 mL de um xarope, com concentração do princípio ativo de 15 mg por mL. Nesse caso, a descrição da apresentação seria: 15MG/ML XPE CT FR VD x 50 ML.

**`QTD_VENDIDA:`** Quantidade vendida de caixas ou frascos do medicamento.<br>
**`UNIDADE_MEDIDA:`** Indica se a quantidade vendida do medicamento foi de caixas ou frascos.<br>
**`CONSELHO_PRESCRITOR:`** Conselho de Classe do profissional que prescreveu o medicamento vendido.<br>
**`UF_CONSELHO_PRESCRITOR:`** Unidade Federativa do Conselho de Classe do profissional que prescreveu o medicamento vendido.<br>
**`TIPO_RECEITUARIO:`** Tipo de receituário utilizado na prescrição. Valores e respectivos tipos de receituário:<br>

1. Receita de Controle Especial em 2 vias (Receita Branca);
2. Notificação de Receita B (Notificação Azul);
3. Notificação de Receita Especial (Notificação Branca);
4. Notificação de Receita A (Notificação Amarela);
5. Receita Antimicrobiano em 2 vias.

**`CID10:`** Classificação Internacional de Doença (aplicável apenas a medicamentos antimicrobianos).<br>
**`SEXO:`** Sexo do paciente (aplicável apenas a medicamentos antimicrobianos). Valor 1 para o sexo masculino, valor 2 para o sexo feminino.<br>
**`IDADE:`** Valor numérico que representa a idade do paciente, em meses ou anos (aplicável apenas a medicamentos antimicrobianos).<br>
**`UNIDADE_IDADE:`** Unidade de medida da idade do paciente, que pode ser em meses ou anos (aplicável apenas a medicamentos antimicrobianos). Valor 1 para unidade de medida em anos, valor 2 para unidade de medida em meses.
<br><br>
**Observação:** Os campos não preenchidos eventualmente encontrados nos arquivos são decorrentes do não preenchimento do referido campo pela farmácia ou drogaria, ou devido ao fato de o campo não se aplicar a determinada categoria. Por exemplo, o campo CID10 é aplicável às vendas de medicamentos antimicrobianos. Ainda assim, mesmo para vendas de medicamentos antimicrobianos, o valor para esse campo pode não ter sido informado.

<br><br>
**Notebook:** [Análise de Vendas Farmacêuticas](https://github.com/wagnermoraesjr/Analise_de_Vendas_Farmaceuticas/blob/main/Projeto_Analise_de_Vendas_Farmaceuticas_github.ipynb)
