# vac-covid_19_3005_SC_c26_c30_c31

# Fonte – OpenDataSus (1)   
# Registros de Vacinação Covid19
# Dados SC – Santa Catarina – Brasil
# Data de download– 30 de maio 2021 as 05horas da manhã.
# Inicial máster File nomeado – sc3005_05am.csv
# Total file size – 1.11 GB = 34 colunas e 2,017,225 de linhas  (2)

# Problema: 

## Inconsistências entre 3 colunas referentes a identificação da covid_19 vacina aplicada ao individuo.
## ••Estas inconsitencias nao permitem identificar com certeza qual foi o fabricante da vacina recebida pelo individuo.••

## coluna 26 - vacina_fabricante_nome
## coluna 30 - vacina_codigo
## coluna 31 - vacina_nome

# Objetivo deste estudo: 

Como projeto de estudo do Modulo 1 do ALURA Bootcamp Data Science, explorar combinação de instrumentos para data parsing e um proof of concept análises para ser usado como modelo de Risk Based Monitoring na gestão do plano de vacinação ao nível das UDVEs catarinenses, seguindo o modelo ICH&GCP (3) usado em estudos clínicos na indústria farmacêutica. 

# Interim results: 

12% dos registros catarinenses (249,437 out of 2 Million) de vacinacao contra o covid-19 na base de dados e data identificados acima, não permitem de confirmar com certeza qual foi o fabricante da vacina tomada pelo individuo. Praticamente 100 % destes registros conflituosos envolvem vacinas da Oxford-Astra Zeneca/ F. Oswaldo Cruz e SINOVAC/BUTANTAN. Lembremos que os intervalos entre as doses 1 e 2 destes fabricantes é totalmente diferente, três meses e um mês, respectivamente. Lembremos também que, devido a problemas de fornecimento das vacinas, o intervalo entre as duas doses foi também estendido para estes dois fabricantes, em algum momento nos últimos meses.

Entre os mais graves problemas que conflitos entre estas três colunas podem gerar, podemos citar:

### Análises de Pharmacovigilancia: por exemplo, avaliacao epidemiologica da frequencia de raro Serious Adverse Event de AVCs como documentados em território europeu (4)

### Compliance: assegurar que os postos de saúde & vacinação sejam capazes de identificar e planejar a planilha de vacinação para dose 2.

### Logistica, Gestão e reabastecimento de stocks a nivel federeal, estadual e municipal dentro do intervalo adequado.


# Método usado para este projeto: 

O método usado foi essentialmente reativo e adaptativo a problemas regionais de eletricidade e/ou internet na região onde resido assim como limitações para tratar files voluminosos com os instrumentos disponíveis. De maneira geral, este projeto teve três fases, cada uma usando um instrumento diferente.

## Fase 1: Terminal Command Line:  como o Colab não aceitava grandes files, usei o Terminal Command Line do meu computador para criar 17 files separados, cada um correspondendo a uma das UDVEs regionais do estado de SC Catarina.

## Fase 2: Usando o Google Drive, Colab e Python – isolei as três colunas mencionadas acima e contabilizei o número de registros para cada uma da combinaçoes existentes entre as três colunas.

## Fase 3: Como meu aprendizado com o Colab&Python ainda está na sua fase inicial e para respeitar o deadline usei o Excel para agrupar os resultados de cada região, contabilizar o número total de registros assim como a percentagem de registros por UDVE com combinações obviamente errôneas.

Informações sobre a Fase 1 e 3 se encontram no Excel file “sc3005_05am - Documentação Github Phases 1 e 3 - amf60 vac-covid_19_3005_SC_c26_c30_c31”

# Comentario:

A construção, ainda em progresso, deste projeto de recursos híbridos para tratamento e análise esta baseado no modelo de Risk Based Monitoring. Permitiu identificar, localizar e comprovar um problema sistêmico (porque identificado em 16 das 17 UDVES) na documentação dos registros de vacinações ao nível de alguns alguns postos de vacinacao&saude no estado de Santa Catarina Brasil. A boa notícia é que este problema parece ser localizado (portanto teoricamente necessitando um simples plano corretivo), pois apenas uma UDVE regional concentra ~ 72% destes registros conflituosos. 

Note que este projeto também está sendo elaborada para documentar, seguindo regras ICH&GCP, para assegurar reproducibility, replicability and generalizibility (5) deste projeto para outros estados brasileiros.

Tenho certeza de que, com ajuda dos Alurienses este projeto evoluirá significativamente durante este Alura Bootcamp DataScience. Talvez venha ajudar a identificar e resolver problemas sistêmicos nos registros de vacinação do covid-19 em outros estados brasileiros. Principalmente porque estas bases de dados irao ficar maiores e mais complexas nos meses a seguir com o aumento de registros e fabricantes de vacina contra o covid-19

Cordialmente,

Aldir MEDEIROS FILHO

*(1) https://opendatasus.saude.gov.br/dataset/covid-19-vacinacao/resource/ef3bd0b8-b605-474b-9ae5-c97390c197a8?view_id=6bf433e7-16ec-4dfa-a725-08db02322bd6 
*(2) O numero de linhas esta relativamente proximo do ultimo DIVE boletim disponivel do dia 26 de Maio que contabilizava 2,263,441 ( http://www.dive.sc.gov.br/index.php/arquivo-noticias/1635-vacinacao-em-sc-2-263-441-doses-da-vacina-contra-a-covid-19-foram-aplicadas-em-sc). E possivel tambem que parte desta diferenca se deva a problemas tecnicos nos ultimos dias (http://www.dive.sc.gov.br/index.php/arquivo-noticias/1639-nota-sobre-dados-do-balanco-parcial-de-vacinacao-contra-a-covid-19-em-santa-catarina)

*(3) https://www.ich.org
*(4) https://www.bbc.com/news/health-56674796)
*(5) https://www.nap.edu/catalog/25303/reproducibility-and-replicability-in-science

