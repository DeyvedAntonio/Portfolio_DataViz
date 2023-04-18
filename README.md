# Portfolio_DataViz
[![](https://img.shields.io/github/license/deyvedantonio/readme_atrativo)](https://github.com/DeyvedAntonio/Portfolio_DataViz/blob/main/LICENSE)

Portfólio para projetos de visualização de dados

## Projeto cotação de moedas

A empresa Sistemas Lotus deseja desenvolver uma ferramenta para acompanhar a cotação de três moedas - Dólar (US$), Euro (€$) e Dólar Canadense (CAD$) - pelo portal de dados abertos do Banco Central do Brasil (BACEN).

## Sobre

Os dados necessários são Disponibilizados pelo Portal de dados abertos do Banco Central por meio da [API](https://olinda.bcb.gov.br/olinda/servico/PTAX/versao/v1/aplicacao#!/recursos/Moedas) e a documentação sobre a API é possível encontrar [aqui](https://olinda.bcb.gov.br/olinda/servico/PTAX/versao/v1/documentacao). O Portal de Dados Abertos do Banco Central é um catálogo de dados abertos, e a partir dele é possível encontrar os locais onde os dados podem ser acessados.

Os códigos dos recursos disponibilizados são: Moedas, CotacaoDolarDia, CotacaoDolarPeriodo, CotacaoMoedaDia, CotacaoMoedaPeriodo.

Os parâmetros são: codigoMoeda, dataInicialCotacao, dataFinalCotacao, $format (formato de retorno que pode ser: json, csv, xml e html) e $select (Propriedades que serão retornadas).

As propriedades retornadas da API são: Cotação de compra, Cotação de venda, data e hora da cotação.

Endereço padrão - https ://olinda.bcb.gov.br/olinda/servico/PTAX/versao/v1/odata/Moedas?$format=json&[Outros Parâmetros].

Exemplo de URL de pesquisa:
<div>
https://olinda.bcb.gov.br/olinda/servico/PTAX/versao/v1/odata/CotacaoMoedaPeriodoFechamento(codigoMoeda=@codigoMoeda,dataInicialCotacao=@dataInicialCotacao,dataFinalCotacao=@dataFinalCotacao)?@codigoMoeda=''&@dataInicialCotacao=''&@dataFinalCotacao=''&$format=text/csv&$select=cotacaoCompra,cotacaoVenda,dataHoraCotacao
</div>

## Layout
<div align="left">
<img src="https://user-images.githubusercontent.com/26858993/159814407-54748ee8-5f67-410f-b36f-a5909212f931.png" width="500px" />
</div>


## Tecnologias utilizadas

### Feramentas
- Power BI Desktop
- API do BACEN

### Subdivisão 2
- tecnologia 2.1
- tecnologia 2.2

## Competências
Informar quais competências.

## Técnicas utilizadas

## Integrações
quais bibliotecas foram utilizadas para integração.

## Escopo da aplicação (opcional)
Casos de usos, cadastros.

## Agradecimentos

### Pessoas
Muito obrigado, Thalita e Nelio, por vocês estarem presentes nessa caminhada.

### Empresas
Muito Obrigado pela dedicação em fornecer materiais de qualidade.
[Data Science Academy](https://www.datascienceacademy.com.br/), [Hashtag Treinamentos](https://www.hashtagtreinamentos.com/), [DATAB](https://datab.com.br/).

## Autor
Deyved Antonio

## Redes Sociais

[Linkedin](https://www.linkedin.com/in/deyved-antonio-161216122/), [Medium](https://medium.com/@deyved.antonio) e [e-mail](deyved.antonio@gmail.com).
