# COVID_Brasil :space_invader: :microscope:

Bem vindo/Bem vinda/Bem vinde! Este repositório está atualmente em **construção** e conterá dados e códigos utilizados para análises da situação brasileira frente à pandemia da COVID-19. Até o momento atual (14/04/2021), se encontra aqui:

1. Código fonte utilizado para estimar de forma mais realística o numero total de óbitos por COVID-19 no Brasil, utilizando dados do portal [Bigdata-covid19](https://bigdata-covid19.icict.fiocruz.br/) da Fiocruz e os dados do [OurWorldInData](https://ourworldindata.org/coronavirus);
2. Os dados baixados do portal [Bigdata-covid19](https://bigdata-covid19.icict.fiocruz.br/), nomeados [fiocruz_sivep_gripe.csv](https://github.com/PedroHPCintra/COVID_Brasil/blob/main/fiocruz_sivep_gripe.csv), contendo os registros de óbitos por síndrome respiratória aguda grave no Brasil, nos anos de 2018, 2019 e 2020;
3. Dados retirados dos boletins epidemiológicos de 2016 e 2017 sobre SRAG no Brasil, nomeados de [SRAG_2016_2017.csv](https://github.com/PedroHPCintra/COVID_Brasil/blob/main/SRAG_2016_2017.csv);
4. Os dados baixados do [OurWorldInData](https://ourworldindata.org/coronavirus), nomeados de [owid-covid-data.csv](https://github.com/PedroHPCintra/COVID_Brasil/blob/main/owid-covid-data.csv), contendo os registros de casos, óbitos, vacinaçes, etc, de todos os países do mundo.

## Utilização do código

Caso queira utilizar o código para rodar uma análise mais recente, baixe este repositório ou use o comando ```git clone``` no terminal do seu computador para clonar este repositório para seu computador. Caso esteja no Linux, rode
```
cd /caminho_ate_a_pasta_onde_se_deseja_baixar
```
em seguida
```
git clone https://github.com/PedroHPCintra/COVID_Brasil.git
```
Uma vez tendo o  repositório, abra o arquivo ```.ipynb``` em seu Jupyter Notebook e acesse os dois sites de referências da Fiocruz e do OurWorldInData para baixar os dados mais recentes. Uma vez baixados, basta atualizar o código para se adaptar aos seus dados mais novos.

### Exemplo:
Caso tenha baixado os dados do OurWorldInData em seu computador, substitua o endereço na função ```pd.read_csv```.
```python
owid = pd.read_csv('home/local de download/nome do arquivo.csv')
```

### Lembrete:
O arquivo .csv baixado pelo portal Fiocruz vem transposto (linhas vem como colunas e colunas como linhas). Para este programa, eu consertei a formatação. Caso baixe os dados mais recentes do portal Fiocruz, note que eles virão no formato

|Semana epidemiológicaobito 2018|1|2|3|4|...|
|:-----------------------------:|:--:|:--:|:--:|:--:|:--:|
|SRAG: óbitosobito 2018|49|91|127|160|...|
|Semana epidemiológicaobito 2019|1|2|3|4|...|
|SRAG: óbitosobito 2019|44|85|130|172|...|

Você deve fazer uma transposição destes dados, ou seja, eles precisam estar na formatação

|Semana epidemiológicaobito 2018|SRAG: óbitosobito 2018|Semana epidemiológicaobito 2019|SRAG: óbitosobito 2019|...|
|:-----------------------------:|:--------------------:|:-----------------------------:|:--------------------:|:--:|
| 1 | 49 | 1 | 44 | ... |
| 2 | 91 | 2 | 85 | ... |
| 3 | 127 | 3 | 130 | ... |
| 4 | 160 | 4 | 172 | ... |
