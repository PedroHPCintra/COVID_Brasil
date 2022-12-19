# COVID_Brasil :space_invader: :microscope:

Bem vindo/Bem vinda/Bem vinde! Este repositório está atualmente em **construção** e conterá dados e códigos utilizados para análises da situação brasileira frente à pandemia da COVID-19. Até o momento atual (14/02/2022), se encontra aqui:

1. Código fonte utilizado para estimar de forma mais realística o numero total de óbitos por COVID-19 no Brasil, utilizando dados do portal [Bigdata-covid19](https://bigdata-covid19.icict.fiocruz.br/) da Fiocruz e os dados do [OurWorldInData](https://ourworldindata.org/coronavirus);
2. Os dados baixados do portal [Bigdata-covid19](https://bigdata-covid19.icict.fiocruz.br/), nomeados [fiocruz_sivep_gripe.csv](https://github.com/PedroHPCintra/COVID_Brasil/blob/main/fiocruz_sivep_gripe.csv), contendo os registros de óbitos por síndrome respiratória aguda grave no Brasil, nos anos de 2018, 2019 e 2020;
3. Dados retirados dos boletins epidemiológicos de 2016 e 2017 sobre SRAG no Brasil, nomeados de [SRAG_2016_2017.csv](https://github.com/PedroHPCintra/COVID_Brasil/blob/main/SRAG_2016_2017.csv);
4. Os dados baixados do [OurWorldInData](https://ourworldindata.org/coronavirus), nomeados de [owid-covid-data.csv](https://github.com/PedroHPCintra/COVID_Brasil/blob/main/owid-covid-data.csv), contendo os registros de casos, óbitos, vacinaçes, etc, de todos os países do mundo.
5. Dados retirados do [nowcasting](https://gitlab.procc.fiocruz.br/lsbastos/nowcasting_data/) que corrige o registro de casos de SRAG devido ao atraso que se tem entre a notificação e a entrada no sistema.

**Atenção, os dados e códigos acima descritos estão desatualizados devido ao período sem dados do Ministério da Saúde, que impossibilitou a continuidade do nowcasting e as estimativas de óbitos por COVID-19**

6. Código e dados para os mapas de vacinação com segunda e terceira dose no Brasil. Este código e os dados estão localizados na pasta ```Cobertura_municipios```;
7. Código para reproduzir a pirâmide de vacinação do Brasil, os dados devem ser extraídos pelo usuário através do [opendatasus](https://opendatasus.saude.gov.br/). Este código está localizado na pasta ```vacinacao```.

## Utilização do código

Caso queira utilizar os códigos para rodar uma análise mais recente, baixe este repositório ou use o comando ```git clone``` no terminal do seu computador para clonar este repositório para seu computador. Caso esteja no Linux, rode
```
cd /caminho_ate_a_pasta_onde_se_deseja_baixar
```
em seguida
```
git clone https://github.com/PedroHPCintra/COVID_Brasil.git
```
Uma vez tendo o  repositório, abra o arquivo ```.ipynb``` em seu Jupyter Notebook e acesse os sites descritos nas referências para baixar os dados que não se encontram junto com este repositório. Uma vez baixados, basta atualizar o código para se adaptar aos seus dados mais novos.
