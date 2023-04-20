# Portfolio_DataViz
[![](https://img.shields.io/github/license/deyvedantonio/readme_atrativo)](https://github.com/DeyvedAntonio/Portfolio_DataViz/blob/main/LICENSE)

> Portfólio para projetos de visualização de dados

## Projeto cotação de moedas

A empresa Sistemas Lotus deseja uma ferramenta para acompanhar a cotação de três moedas - Dólar (US$), Euro (€$) e Dólar Canadense (CAD$) - pelo portal de dados abertos do Banco Central do Brasil (BACEN).

## Sobre

Os dados necessários são disponibilizados pelo Portal de dados abertos do Banco Central por meio da [API](https://olinda.bcb.gov.br/olinda/servico/PTAX/versao/v1/aplicacao#!/recursos/Moedas) e a documentação sobre a API é possível encontrar [aqui](https://olinda.bcb.gov.br/olinda/servico/PTAX/versao/v1/documentacao). O Portal de Dados Abertos do Banco Central é um catálogo de dados abertos, e a partir dele é possível encontrar os locais onde os dados podem ser acessados.

### Etapas desenvolvidas para resolver o problema

- Entender os dados:

  * É necessário entender os parâmetros para buscar os dados na API de forma correta.
  * Os códigos dos recursos disponibilizados são: Moedas, CotacaoDolarDia, CotacaoDolarPeriodo, CotacaoMoedaDia, CotacaoMoedaPeriodo.
  * Os parâmetros são: codigoMoeda, dataInicialCotacao, dataFinalCotacao, $format (formato de retorno que pode ser: json, csv, xml e html) e $select (Propriedades que serão retornadas).
  * As propriedades retornadas da API são: Cotação de compra, Cotação de venda, data e hora da cotação e tipo de boletim (que pode ser: abertura, intermediário e fechamento).
  * Endereço padrão - https ://olinda.bcb.gov.br/olinda/servico/PTAX/versao/v1/odata/Moedas?$format=json&[Outros Parâmetros].

- Determinar período de cotação dos dados:

  * Um intervalo de 12 meses. formato MM-DD-AAAA
  * Data inicial cotação: 03/31/2022
  * Data final cotação: 03/31/2023

- Determinar o nível da granularidade dos dados:

  * Uma vez por dia.
  * tipo de boletim: fechamento

- Pipeline de Dados:

  * Criação da URL para extração dos dados na API;
  * Formato de retorno será em CSV;
  * Transfomação e carregamento será direto no Power BI.
 
- URL para extração de dado na API:
  * Moeda Euro:
    <p>
    https://olinda.bcb.gov.br/olinda/servico/PTAX/versao/v1/odata/CotacaoMoedaPeriodo(moeda=@moeda,dataInicial=@dataInicial,dataFinalCotacao=@dataFinalCotacao)?@moeda='EUR'&@dataInicial='03-03-2022'&@dataFinalCotacao='03-31-2023'&$top=10000&$format=text/csv&$select=cotacaoCompra,cotacaoVenda,dataHoraCotacao,tipoBoletim
    </>>

  * Extração dos dados na API

    <div align="center">
    <img src="https://github.com/DeyvedAntonio/Portfolio_DataViz/blob/main/Imagens/euro_url.png" width="500px" />
    </div>
    <div align="center">
    <img src="https://github.com/DeyvedAntonio/Portfolio_DataViz/blob/main/Imagens/euro_access.png" width="500px" />
    </div>
    <div align="center">
    <img src="https://github.com/DeyvedAntonio/Portfolio_DataViz/blob/main/Imagens/euro_resultado.png" width="500px" />
    </div>

 * Transfomações aplicadas nos dados

    - Renomear a base de dados
    - Converter as colunas cotacaoCompra e cotacaoVenda do tipo decimal para o tipo monetário;
    - Filtrar a coluna tipoBoletim por fechamento;
    - Excluir a coluna tipoBoletim;
 
## Layout

 <div align="center">
 <img src="https://github.com/DeyvedAntonio/Portfolio_DataViz/blob/main/Imagens/layout_0.0.1.png" width="500px" />
 </div>

## Tecnologias utilizadas

### Feramentas

- Power BI Desktop (é um aplicativo gratuito que pode ser instalado no computador local e que permite que você se conecte aos seus dados, transforme-os e visualize-os.)
- API (expressão inglesa Application Programming Interface que, traduzida para o português, pode ser compreendida como uma interface de programação de aplicação)

### Tipo de arquivos

- CSV (são arquivos de texto de formato regulamentado pelo RFC 4180, que faz uma ordenação de bytes ou um formato de terminador de linha, separando valores com vírgulas.)

## Competências

- Extração de dados por meio de API;
- Transformação de dados;
- Carregar dados;
- Exibição dos resultados por meio de relatórios.

## Técnicas utilizadas

- Processos de ETL (Extrair, transformar e carregar é o processo que as organizações orientadas a dados usam para coletar dados de várias fontes e reuni-los para dar suporte à descoberta, à geração de relatórios, à análise e à tomada de decisões);
- Storytelling (é a arte de contar histórias usando técnicas inspiradas em roteiristas e escritores para transmitir uma mensagem de forma inesquecível).

## Agradecimentos

### Pessoas
Muito obrigado, Thalita e Nelio, por vocês estarem presentes nessa caminhada.

### Empresas
Muito Obrigado pela dedicação em fornecer materiais de qualidade.
[Data Science Academy](https://www.datascienceacademy.com.br/), [Hashtag Treinamentos](https://www.hashtagtreinamentos.com/), [DATAB](https://datab.com.br/).

## Autor
Deyved Antonio

## Redes sociais e Contatos

[Linkedin](https://www.linkedin.com/in/deyved-antonio-161216122/), [Medium](https://medium.com/@deyved.antonio) e [e-mail](deyved.antonio@gmail.com).
