# Leia-me :open_book:

:smile: Olá, aqui se encontra disponibilizado o código fonte, bem como os dados, utilizado para gerar os mapas de cobertura vacinal de 2ª dose por município nos estados do Brasil. As fontes para ambos os estados encontram-se listadas abaixo, sinta-se livre para baixar os dados mais recentes em seu computador
e utilizar o script em ```python``` para gerar as imagens em ```.html```.

Tento atualizar estes dados toda terça-feira, adquirindo assim os dados referentes até a segunda feira. A versão mais recente dos dados foi baixada no dai 18/01/2022. Os dados para produção dos mapas de vacinação vem do [LocalizaSUS](https://infoms.saude.gov.br/extensions/DEMAS_C19_Vacina_v2/DEMAS_C19_Vacina_v2.html).

**Atenção**

:world_map: Caso você só esteja aqui para baixar e visualizar os mapas de cobertura vacinal nestes estados, os arquivos estão na pasta ```Maps```. Os
nomes dos arquivos são:
- Mapas dos estados: ```vaccine_SIGLA_2_dose.html```
- Mapa de SP, MG, SC e TO: ```vaccine_SILGA_dose.zip```

Os mapas de São Paulo, Minas Gerais, Santa Catarina e Tocantis são grandes demais para fazer upload aqui no github, sendo assim, é necessária realizar sua compressão em um ```.zip```, basta baixar o arquivo e descomprimir para poder abrir o mapa em seu computador.

:chart_with_upwards_trend: Já caso você esteja aqui para ver a distribuição de coberturas vacinais nos municípios,
ela se encontra na pasta ```Distributions```. De forma análoga ao mapa de vacinação, você os estados estão identificados pela sigla no nome do arquivo.

## Código

Caso queira reproduzir os mapas em seu computador usando o código que uso, o arquivo é um Jupyter Notebook chamado ```Homogeneidade_BR_vacinacao.ipynb```. Nele, eu uso o google colab como repositório para os arquivos shapefiles de Minas Gerais, Santa Catarina e Tocantins, pois eles são grandes demais para colocar no github. Sendo assim você precisará baixá-los em seu computador através do [IBGE Malhas Municípais](https://www.ibge.gov.br/geociencias/organizacao-do-territorio/malhas-territoriais/15774-malhas.html?=&t=downloads). Após ter baixado, substitua a linha de código

```python
if state == 'MG' or state == 'SC' or state == 'TO':
    !unzip 'gdrive/MyDrive/Brasil/Malha_municipal/{state}_Municipios_2020.zip'
```

por


```python
if state == 'MG' or state == 'SC' or state == 'TO':
    !unzip 'Endereço onde o arquivo está salvo/{state}_Municipios_2020.zip'
```

Neste código, são gerados os mapas de vacinação dos municípios de cada estado, uma distribuição de coberturas vacinais para cada estado, um mapa de homogeneidade vacinal para o Brasil e um mapa de cobertura vacinal por mesorregiões no Brasil. Para esté último também será necessário baixar o arquivo ```Mesorregioes_e_municipios.csv``` para rodar o código em seu computador.

## Fontes

Dados vacinação para os estados e municípios: [https://infoms.saude.gov.br/extensions/DEMAS_C19_Vacina_v2/DEMAS_C19_Vacina_v2.html](https://infoms.saude.gov.br/extensions/DEMAS_C19_Vacina_v2/DEMAS_C19_Vacina_v2.html)
