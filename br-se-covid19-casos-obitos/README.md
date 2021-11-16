# Dados de Casos e Óbitos

Nesta pasta você encontra os scripts de processamento dos dados de casose  óbitos do Estado de Sergipe. Os dados foram coletados direto do site do [https://brasio.io](brasil.io) que coleta, organiza e publica dados de casos e óbitos de todo o Brasil a nível de município. Os dados utilizados aqui são apenas um recorte dos dados completos filtrando pelo estado de Sergipe. O site atualiza diariamente os dados.

## Organização 

Essa pasta está organizada na seguinte estrutura: 

* `code`: pasta com os scripts de processamento. 
* `input`: pasta com os dados originais e sem alterações que foram extraídos direto do site https://todoscontraocorona.net.br/. Essa pasta também contém outros dados de entrada que são usados no processamento. Esses arquivos nunca são modificados. 
* `output`: pasta com os arquivos de saída resultados da etapa de processamento. Esses arquivos não são modificados manualmente também. Sempre são gerados a partir dos scripts de processamento. 

## Estrutura dos Arquivos 

### Arquivo `municipios_casos_obitos.csv`

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

