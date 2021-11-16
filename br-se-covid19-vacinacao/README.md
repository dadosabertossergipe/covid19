# Dados da Vacinação

Nesta pasta você encontra os scripts de processamento dos dados de vacinação do Estado de Sergipe. Os dados são disponibilizados pela secretaria estadual de saúde através do link: https://todoscontraocorona.net.br/. Os boletins são divulgados quase que diariamente com as informações de doses aplicadas e enviadas por município e por grupo vacinado. Além disso, os arquivos possuem informações sobre a cobertura vacinal. 

No entanto, o formato disponibilizado além de ser proprietário, sofreu muitas alterações desde do início da vacinação. Isso dificulta a análise desses dados por meios automatizados. Os scripts desta pastam processam os arquivos originais e gera um arquivo em formato aberto (.csv) com nome das colunas padronizadas com as informações do histórico de vacinação para todos os 75 municípios do estado. 

O arquivo atualmente conta com as seguintes informações: 

* Data: data de divulgação do boletim
* Código do Município: Código de 7 dígitos do IBGE que identifica cada município.
* Nome do Município
* Total de doses recebidas pelo município: essa infomação está distribuída de acordo com o tipo de dose aplicada: dose 1, dose 2, dose única, dose de reforço.
* Total de doses aplicadas pelo município: essa informação está distribuída de acordo com o tipo de dose aplicada: dose 1, dose 2, dose única,, dose de reforço. 

Mais detalhes sobre as colunas pode ser encontrada no final desse README. 

## Organização 

Essa pasta está organizada na seguinte estrutura: 

* `code`: pasta com os scripts de processamento. 
* `input`: pasta com os dados originais e sem alterações que foram extraídos direto do site https://todoscontraocorona.net.br/. Essa pasta também contém outros dados de entrada que são usados no processamento. Esses arquivos nunca são modificados. 
* `output`: pasta com os arquivos de saída resultados da etapa de processamento. Esses arquivos não são modificados manualmente também. Sempre são gerados a partir dos scripts de processamento. 
* `tmp`: arquivos temporários gerados durante a etapa de processamento dos dados. 

## Estrutura dos Arquivos 

### Arquivo `municipio_total.csv`

| Coluna | Descricao | Formato | Observação |
| -------| --------- | ------- | ---------- |
| data | data de divulgacao do boletim | String no formato `YYYY-MM-DD` | |
| codigo_municipio | código de identificação do munícipio de acordo com a classificação do IBGE | Número inteiro de 7 dígitos | |
| nome_municipio | nome do município | String | |
| enviadas_dose1 | total de doses enviadas ao município pela secretaria estadual para aplicação da primeira dose | Número inteiro | Esses dados só estão disponíveis a partir de 09/02/21  |
| enviadas_dose2 | total de doses enviadas ao município pela secretaria estadual para aplicação da segunda dose | Número inteiro | |
| enviadas_dose_unica | total de doses enviadas ao município pela secretaria estadual para aplicação da dose única | Número inteiro | |
| enviadas_dose_reforco | total de doses enviadas ao município pela secretaria estadual para aplicação da dose de reforço | Número inteiro | |
| aplicadas_dose1 | total de doses (primeira dose) aplicadas pelo município | Número inteiro | |
| aplicadas_dose2 | total de doses (segunda dose) aplicadas pelo município | Número inteiro | |
| aplicadas_dose_unica | total de doses (dose única) aplicadas pelo município | Número inteiro | |
| aplicadas_dose_reforco | total de doses (dose de reforço) aplicadas pelo município | Número inteiro | |

