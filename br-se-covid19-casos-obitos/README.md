# Dados de Casos e Óbitos

Nesta pasta você encontra os scripts de processamento dos dados de casos e  óbitos do Estado de Sergipe. Os dados foram coletados direto do site do [https://brasio.io](brasil.io) que coleta, organiza e publica dados de casos e óbitos de todo o Brasil a nível de município. Os dados utilizados aqui são apenas um recorte dos dados completos filtrando pelo estado de Sergipe. O site atualiza diariamente os dados.

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
| casos confirmados_total | total de casos confirmados no município.  | Número inteiro | Esses dados são acumulativos. Ou seja, o valor de um dia representa o total de casos registrados até o dia anterior mais o total registrado no dia. |
| casos_confirmados_diarios | total de casos confirmados naquele dia. | Número inteiro | |
| obitos_confirmados_total | total de óbitos confirmados no município. | Número inteiro | Esses dados são acumulativos. Ou seja, o valor de um dia representa o total de óbitos registrados até o dia anterior mais o total registrado no dia. |
| obitos_confirmados_diarios | total de óbitos confirmados naquele dia. | Número inteiro | |
| casos_media_movel | média móvel de 7 dias calculada a partir do campo `casos_confirmados_diarios` | Número inteiro | A média móvel é calculada dentro de cada município.  |
| obitos_media_movel | média móvel de 7 dias calculada a partir do campo `obitos_confirmados_diarios` | Número inteiro | A média móvel é calculada dentro de cada município. |