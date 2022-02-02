# Dados de Casos e Óbitos

Nesta pasta você encontra os scripts de processamento dos dados de casos e óbitos do Estado de Sergipe. Atualmente, os dados estão sendo extraídos do site [brasil.io](https://brasil.io). Apenas os dados total do estado estão sendo utilizados. Foi observado uma desatualização dos dados por município na plataforma do brasil.io. 

Ações para obter esse dados por município estão sendo elaborados e em breve, serão atualizadas nesta página. Por enquanto, apenas filtramos da plataforma do braisl.io os dados de interesse.


## Organização 

Essa pasta está organizada na seguinte estrutura: 

* `code`: pasta com os scripts de processamento. 
* `input`: pasta com os dados originais e sem alterações que foram extraídos direto do site brasil. Estes arquivos não são modificados manualmente. Esta pasta não está no repositório por conta do tamanho do arquivo do **brasil.io**. Quem deseja reproduzir, basta criar dentro da pasta `input` a pasta `brasilio` e colocar o arquivo `casos_full.csv` que pode ser baixado no link: https://brasil.io/dataset/covid19/files/.
* `output`: pasta com os arquivos de saída resultados da etapa de processamento. Esses arquivos não são modificados manualmente também. Sempre são gerados a partir dos scripts de processamento. 

## Estrutura dos Arquivos 

### Arquivo `se_covid19_casos_obitos.csv`

| Coluna | Descricao | Formato | Observação |
| -------| --------- | ------- | ---------- |
| data | data de divulgacao do boletim | String no formato `YYYY-MM-DD` | |
| semana_epidemiologica | semana epidemiológica de registro dos números | String no formato YYYYSS, onde SS é a semana. | |
| total_casos_confirmados | total de casos confirmados acumulados até a data | Número Inteiro | |
|  total_obitos_confirmados | total de óbitos confirmados acumulados até a data | Número inteiro |  |
| diario_casos_confirmados | total de casos confirmados na data | Número inteiro | |
| diario_obitos_confirmados | total de óbitos confirmados na data | Número inteiro | |
| media_movel7_casos | Média móvel de 7 dias do número de casos confirmados | Número real | |
| media_movel7_obitos | Média móvel de 7 dias do número de óbitos confirmados | Número real | |