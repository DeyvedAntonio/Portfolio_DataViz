# Portfolio_DataViz
[![](https://img.shields.io/github/license/deyvedantonio/readme_atrativo)](https://github.com/DeyvedAntonio/Portfolio_DataViz/blob/main/LICENSE)

Portfólio para projetos de visualização de dados

## Projeto cotação de moedas

A empresa Sistemas Lotus deseja desenvolver uma ferramenta para acompanhar a cotação de três moedas - Dólar (US$), Euro (€$) e Dólar Canadense (CAD$) - pelo portal de dados abertos do Banco Central do Brasil (BACEN).

## Sobre

Os dados necessários são disponibilizados pelo Portal de dados abertos do Banco Central por meio da [API](https://olinda.bcb.gov.br/olinda/servico/PTAX/versao/v1/aplicacao#!/recursos/Moedas) e a documentação sobre a API é possível encontrar [aqui](https://olinda.bcb.gov.br/olinda/servico/PTAX/versao/v1/documentacao). O Portal de Dados Abertos do Banco Central é um catálogo de dados abertos, e a partir dele é possível encontrar os locais onde os dados podem ser acessados.


### Etapas desenvolvidas para resolver o problema

- Entender os dados:

  * É necessário entender os parâmetros para buscar os dados na API de forma correta.
  * Os códigos dos recursos disponibilizados são: Moedas, CotacaoDolarDia, CotacaoDolarPeriodo, CotacaoMoedaDia, CotacaoMoedaPeriodo.
  * Os parâmetros são: codigoMoeda, dataInicialCotacao, dataFinalCotacao, $format (formato de retorno que pode ser: json, csv, xml e html) e $select (Propriedades que serão retornadas).
  * As propriedades retornadas da API são: Cotação de compra, Cotação de venda, data e hora da cotação.
  * Endereço padrão - https ://olinda.bcb.gov.br/olinda/servico/PTAX/versao/v1/odata/Moedas?$format=json&[Outros Parâmetros].

- Determinar período de cotação dos dados:

  * Um intervalo de 12 meses.

- Determinar o nível da granularidade dos dados:

  * Uma vez por dia.

## Layout

<div align="left">
<img src="https://user-images.githubusercontent.com/26858993/159814407-54748ee8-5f67-410f-b36f-a5909212f931.png" width="500px" />
</div>

## Tecnologias utilizadas

### Feramentas

- Power BI Desktop (é um aplicativo gratuito que pode ser instalado no computador local e que permite que você se conecte aos seus dados, transforme-os e visualize-os.)
- API (expressão inglesa Application Programming Interface que, traduzida para o português, pode ser compreendida como uma interface de programação de aplicação)

### Tipo de arquivos

- CSV (são arquivos de texto de formato regulamentado pelo RFC 4180, que faz uma ordenação de bytes ou um formato de terminador de linha, separando valores com vírgulas.)

## Competências

- Extração de dados por meio de URL;
- Transformação de dados;
- Carregar dados;
- Exibição dos resultados por meio de gráficos.

## Técnicas utilizadas

Processos de ETL (Extrair, transformar e carregar é o processo que as organizações orientadas a dados usam para coletar dados de várias fontes e reuni-los para dar suporte à descoberta, à geração de relatórios, à análise e à tomada de decisões).

## Agradecimentos

### Pessoas
Muito obrigado, Thalita e Nelio, por vocês estarem presentes nessa caminhada.

### Empresas
Muito Obrigado pela dedicação em fornecer materiais de qualidade.
[Data Science Academy](https://www.datascienceacademy.com.br/), [Hashtag Treinamentos](https://www.hashtagtreinamentos.com/), [DATAB](https://datab.com.br/).

## Autor
Deyved Antonio

## Contatos

[Linkedin](https://www.linkedin.com/in/deyved-antonio-161216122/), [Medium](https://medium.com/@deyved.antonio) e [e-mail](deyved.antonio@gmail.com).
