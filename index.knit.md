--- 
title: "Software R: An�lise estat�stica de dados utilizando um programa livre"
author: 
- Felipe Micail da Silva Smolski
- Iara Denise Endruweit Battisti
date: "2018-12-10"
site: bookdown::bookdown_site
documentclass: book
bibliography: [book.bib, packages.bib]
biblio-style: authoryear
link-citations: yes
github-repo: rstub/bookdown-chapterbib
url: 'http\://rstub.github.io/bookdown-chapterbib/'
description: "Curso de an�lise estat�stica com R da UFFS Cerro Largo - RS"
fontsize: 12pt
lang: pt-Br
always_allow_html: yes
classoption: oneside
---





# Apresenta��o {-}

A necessidade de flexibilidade e robustez para a an�lise estat�stica fez com que fosse criado, na d�cada de 1990, a linguagem de programa��o R. Capitaneado pelos desenvolvedores Ross Ihaka e Robert Gentleman, dois estat�sticos da Universidade de Auckland na Nova Zel�ndia, o projeto foi uma grande evolu��o para a an�lise de dados. A partir de ent�o, a ideia inicial de proporcionar autonomia ao pesquisador, viu na expans�o do acesso � internet uma oportunidade para que a pesquisa cient�fica se tornasse cada vez mais colaborativa. Ao mesmo tempo, os c�digos e rotinas se tornaram facilmente disponibiliz�veis na rede, aumentando a reprodu��o e replica��o dos estudos, pr�ticas estas que podem tornar as an�lises mais confi�veis.

A linguagem de programa��o R trouxe consigo in�meras vantagens aos pesquisadores. Dentre elas, pode-se dizer primeiramente que, basicamente o R trabalha com uma extensa rela��o de modelos estat�sticos, que v�o desde a modelagem linear e n�o-linear, a an�lise de s�ries temporais, os testes estat�sticos cl�ssicos, an�lise de grupamento e classifica��o, etc. N�o bastasse este fato, � poss�vel a apresenta��o gr�fica dos resultados contando com variadas t�cnicas, passando tamb�m pela cria��o e manipula��o de mapas.

Outra quest�o importante � que o R possui uma comunidade ativa de desenvolvedores, que se expande regularmente. Isto faz com que as t�cnicas de an�lise de dados atinjam pesquisadores de variadas disciplinas ao longo do planeta. Inclusive, concebe que o desenvolvimento dos pacotes melhorem constantemente. No ano de 2018, j� haviam mais de 12.700 pacotes disponibilizados. N�o menos importante, talvez o essencial: o programa � livre, ao passo que entrega o estado da arte da estat�stica ao usu�rio.

Outro progresso significativo na utiliza��o do R foi a cria��o do *software* RStudio, a partir de 2010. Este, por sua vez, se configura em um ambiente integrado com o R e com in�meras linguagens de marca��o de texto (exemplos LaTeX, Markdown, HTML). Possui igualmente vers�o livre que disponibiliza ao pesquisador a execu��o, guarda, retomada e manipula��o dos c�digos de programa��o diretamente em seu console, bem como a administra��o de diret�rios de trabalhos e projetos.

O material aqui criado � destinado n�o somente a alunos de gradua��o, p�s-gradua��o, professores e pesquisadores acad�micos, mas tamb�m para qualquer indiv�duo interessado no aprendizado inicial sobre a utiliza��o de t�cnicas estat�sticas com o R. Inclusive, com o objetivo de alcan�ar um p�blico das mais variadas �reas do conhecimento, esta obra foi elaborada com exemplos gerais, a serem absorvidos em um momento inicial do estudante. Assim, possui a base para continuar estudos posteriores em estat�stica e no *software* RStudio. O sistema operacional aqui utilizado � o Windows 10. Importante mencionar que este livro origionu-se de projeto de extens�o aprovado no Edital de Apoio a Programas de Extens�o (N� 522/GR/UFFS/2016) da Universidade Federal da Fronteira Sul (UFFS).

Este livro est� organizado da seguinte maneira: no cap�tulo [1](#intro) [**Primeiros Passos com o R**], busca-se instruir o pesquisador para a instala��o dos programas necess�rios para acessar o ambiente de programa��o, bem como orientar sobre a usabilidade do programa em suas fun��es b�sicas de carregamento de bases de dados, cria��o de objetos e princ�pios de manipula��o. 

J� no cap�tulo [2](#desc) [**Estat�stica Descritiva**], leva o leitor ao encontro das t�cnicas b�sicas para descrever as vari�veis em bancos de dados, como exemplos a m�dia, m�nima, m�xima, desvio padr�o, os quartis e tamb�m, apresentar os princ�pios dos elementos gr�ficos de apresenta��o dos dados. 

O cap�tulo [3](#inf) [**Estat�stica Inferencial**] tratar� dos m�todos de determina��o de intervalos de confian�a (m�dia e propor��o), testes de hip�teses (verificar a normalidade dos dados) e das compara��es entre m�dias de amostras dependentes e independentes. 

No cap�tulo [4](#qui) [**Teste de Qui-Quadrado**], ser�o abordadas as referidas t�cnicas para verifica��o de asssocia��o entre duas vari�veis qualitativas e de ader�ncia a uma distribui��o.

No cap�tulo [5](#reg) [**Modelos de Regress�o**] ser�o introduzidos os conhecimentos sobre as t�cnicas de an�lise de correla��o e regress�o linear simples, bem como sobre o diagrama de dispers�o, m�todo dos m�nimos quadrados, an�lise de vari�ncia, coeficiente e intervalo de predi��o, da an�lise dos res�duos e dos princ�pios de regress�o m�ltipla.

A cria��o de documentos din�micos utilizando o RStudio ser� tratada no cap�tulo [6](#rmark) [**RMarkdown**]. O pesquisador poder� conhecer as formas de integrar a programa��o no R e a manipula��o de bases de dados, criando, compilando e configurando relat�rios finais em diversos formatos (HTML, PDF e Word/Libre/Open Office).

Boa leitura!

# Introdu��o{#intro}

*Felipe Micail da Silva Smolski*

*Djaina Sibiani Rieger*

\begin{flushright}
\emph{}

\emph{}
\end{flushright}

O R � um ambiente voltado para an�lise de dados com o uso de uma linguagem de programa��o, frente a isso um conhecimento pr�vio dos pr�ncipios de programa��o facilita a compreens�o da condu��o das an�lises aplicadas no software. Entretanto, n�o � pr�-requisito. Neste cap�tulo abordaremos os primeiros passos para o emprego da linguagem de programa��o R utilizando uma interface "amig�vel" - o software RStudio. Al�m disso, ser�o apresentados os comandos b�sicos para a manipula��o de dados dentro do RStudio.


## Download e instala��o do R e Rstudio


**R**: <http://www.r-project.org>. Clique em Download (CRAN) - escolha o link de um reposit�rio - clique no link do sistema operacional (Linux, Mac ou Windows) - clique em *install R for de first time - Download*. 

**RStudio**: <http://www.rstudio.com/products/rstudio/download>. Em RStudio Desktop, escolha a vers�o *free*, seguidas da op��o do sistema operacional do usu�rio.

Lembrando que:

- R � o software;
- RStudio � uma ferramenta amig�vel para o R.


## Pain�is

O RStudio � a interface que faz com que seja mais f�cil a utiliza��o da programa��o em R. 

<div class="figure" style="text-align: center">
<img src="paineis.png" alt="Pain�is do Rstudio" width="80%" />
<p class="caption">(\#fig:paineis1)Pain�is do Rstudio</p>
</div>
Fonte: Elaborado pelo(s) autor(es).

- **Fonte/Editor de Scripts**: se constitui do ambiente onde ser�o abertos os scripts previamente salvos nos mais diversos formatos ou mesmo sendo o local de visualiza��o das bases de dados.
- **Console**: local onde ser� efetuada a digita��o das linhas de c�digo que ser�o interpretadas pelo R.
- **Ambiente e Hist�rico**: o ambiente ser� visualizado os objetos criados ou carregados durante a se��o e; a aba History retoma os scripts digitados no console.
- **Plots/arquivos/Pacotes**: local onde podem ser acessados os arquivos salvos no computador pela aba *files*; a aba *Plots* carrega os gr�ficos e plotagens; a aba *Packages* cont�m os pacotes instalados em seu computador, onde s�o ativados ou instalados novos; em *Help* constam as ajudas e explica��es dos pacotes e; *Viewer* vizualiza documentos do tipo html.

## Help

Acessamos a ajuda do RStudio por meio do comando `help()`, atrav�s da aba "Help" ou ao clicar no nome do pacote. Pode-se digitar a ajuda que usu�rio necessita (exemplo `help("summary")`), ou diretamente no colsole digitamos ? e a fun��o desejada, exemplo: `?mean`.

## Instala��o de pacotes

Em alguns situa��es, o uso de pacotes pode dar ao trabalho mais praticidade, e para isso se faz necess�rio efetuar a sua instala��o. Precisamos ir at� o painel dos pacotes em *packages*, selecionar a op��o instalar e inserir o nome do pacote desejado na janela indicada. Ao selecionar a op��o instalar, no console receberemos informa��es do procedimento e do sucesso do mesmo. 


<div class="figure" style="text-align: center">
<img src="pacotes1.png" alt="Instala��o de pacotes" width="80%" />
<p class="caption">(\#fig:pacotes1)Instala��o de pacotes</p>
</div>

Fonte: Elaborado pelo(s) autor(es).

<div class="figure" style="text-align: center">
<img src="pacotes2.png" alt="Caixa de informa��o de pacote a ser instalado" width="80%" />
<p class="caption">(\#fig:pacotes2)Caixa de informa��o de pacote a ser instalado</p>
</div>

Fonte: Elaborado pelo(s) autor(es)

A mesma fun��o, para instala��o de um pacote, pode ser efetuada diretamente via console: `install.packages("pacote")`. � importante ressaltar a fun��o `library(nomedopacote)` que � utilizada no console para informar ao R e "carregar" o pacote que o usu�rio ir� utilizar. Podem ser instalados mais de um pacote ao mesmo tempo, como no exemplo:


`install.packages(c("readr", "readxl"))`

## Abrir arquivo de dados

Dispondo de um banco de dados em uma planilha eletr�nica (LibreOffice Calc ou EXCEL), neste caso ser� utilizado o arquivo  [�rvores](https://github.com/Smolski/softwarelivrer/raw/master/basico/arvores.xlsx) como exemplo o banco de dados. Os dados derivam de uma pesquisa com esp�cies de �rvores registrando as vari�veis di�metro altura do peito (DAP) e altura. Dados cedidos pela professora Tatiane Chassot.

Pode-se utilizar a linha de comando para carregar os arquivos de dados, da seguinte forma:

`library(readxl)`

`nome.objeto.xls = read_excel("d:/arvores.xls")`

Outras op��es de arquivos podem ser carregados no RStudio, como por exemplo arquivos de texto (.txt ou .csv), arquivos derivados do excel (.xls ou .xlsx), arquivos de dados do SPSS (.sav), do *software* SAS (.sas7bdat) e do STATA (.dta). A instala��o de alguns pacotes � requerida, dependendo da origem da base de dados, como por exemplo o `readxl`, `readr` e `haven`, como os exemplos abaixo:

`library(readr)`

`nomeobjeto = read.csv("d:/arvores.csv")`

`library(haven)` 

`nomeobjeto = read_sav("d:/arvores.sav")`

`nomeobjeto = read_dta("d:/arvores.dta")`

`nomeobjeto = read_sas("d:/arvores.sas7bdat")`

Outras op��es podem ser comandadas dentro destes comando para abertura de arquivos, como por exemplo, um arquivo csv em que esteja separado por v�rgulas pode ser lido como:

`read.csv("d:/arvores.csv", sep=",")`

O comando `header=TRUE` diz que a primeira linha do arquivo cont�m o cabe�alho; `skip=4` faz com que sejam ignoradas as 4 primeiras linhas.

A fun��o `load()` (exemplo: `load("base.RData")`) pode ser utilizada para carregar as bases de dados salvas com a fun��o `save()`, que ser� descrita no subcap�tulo a seguir.

Outra op��o � o carregamento das bases de dados manualmente pelo caminho *Envoirment $>$ Import Dataset*, escolhendo o tipo de arquivo:

<div class="figure" style="text-align: center">
<img src="r3.png" alt="Aba Import Dataset" width="80%" />
<p class="caption">(\#fig:r3)Aba Import Dataset</p>
</div>

Fonte: Elaborado pelo(s) autor(es).

Na caixa correspondente a File/Url se insere o endere�o virtual ou o local onde se encontra o arquivo. Ao importar os dados, carrega-se um objeto criado com as informa��es contidas no arquivo. No nosso exeplo, carregamos a planilha arvores (arquivo .xls) como mostra a Figura \@ref(fig:r4), derivado do caminho "Import Dataset $>$ From Excel" do Environment.

<div class="figure" style="text-align: center">
<img src="r4.png" alt="Caixa de informa��es do Import Data" width="80%" />
<p class="caption">(\#fig:r4)Caixa de informa��es do Import Data</p>
</div>
Fonte: Elaborado pelo(s) autor(es).

O campo *Code Preview* mostra o comando que est� sendo criado para a importa��o destes dados. Em *Import Options*, delimita-se op��es do objeto como o nome (*name*), o n�mero m�ximo de linhas (*Max Rows*), quantas linhas ser�o puladas na importa��o do arquivo (*Skip*), o tratamento das c�lulas em branco (*NA*) e se a primeira linha cont�m os nomes (*Firts Row as Names*).

Com rela��o � importa��o de arquivos de texto separado por caracteres (.csv), ela se d� via "Import Dataset $>$ From Text (readr)" do Environment. Constam algumas solicita��es diferentes a serem determinadas pelo usu�rio no campo *Import Options*, conforme mostra a Figura \@ref(fig:r4csv). Uma quest�o importante � a op��o *Delimiter*, a qual o pesquisador tem que prestar aten��o quando o arquivo est� separado por v�rgulas (*Comma*), ponto e v�rgula (*Semicolon*) ou outro tipo de caractere. A op��o *Locale $>$ Configure...* oportuniza determinar os tipos de marca decimal e codifica��o de textos, por exemplo.

<div class="figure" style="text-align: center">
<img src="r4csv.png" alt="Op��es da importa��o de arquivos .csv" width="80%" />
<p class="caption">(\#fig:r4csv)Op��es da importa��o de arquivos .csv</p>
</div>

Fonte: Elaborado pelo(s) autor(es)

Importante mencionar que em ambos os casos de importa��o, no campo *Dada Preview* onde constam os dados do arquivo a ser importado, � poss�vel determinar o tipo de dado que cada "coluna" cont�m. Isto � extremamente importante, pois campos que possuem n�meros, que ser�o posteriormente utilizados em opera��es aritm�ticas, por exemplo, devem ser configurados como tal. No entanto, como ser� visto adiante, a altera��o do tipo do dado tamb�m pode ser feita posteriormente sem problema algum.

Alguns tipos de dados:

- **Numeric**: n�meros, valores decimais em geral (`5.4`).
- **Integer**: n�meros (`4`).
- **Character**: vari�vel de texto, ou *string* (`casa`).
- **Double**: cria um vetor de precis�o dupla, que abarca os n�meros.
- **Logical**: operadores booleanos (`TRUE, FALSE`).
- **Date**: op��o para datas.
- **Time**: vetor para s�ries de tempo.
- **Factor**: vari�vel nominal, inclusive como fator ordenado, representam categorias.

Ainda, � poss�vel importar objetos utilizando arquivos hospedados em links da internet, por exemplo o comando  `source("http://www.openintro.org/stat/data/cdc.R")` utiliza a fun��o `source()` para carregar um objeto do R denominado cdc ("cdc.R").

## Salvar arquivo de dados

O banco de dados que o R armazena na mem�ria pode ser salvo, junto com todo o ambiente, usando o �cone de disquete na aba "Environment" (salva como arquivo .RData), e depois carregado pelo �cone de pasta (Abrir dados...) na mesma aba. Desta forma, salvar� todos os objetos criados no ambiente de trabalho.

<div class="figure" style="text-align: center">
<img src="r6.png" alt="Atalho para abrir e salvar arquivo de dados" width="80%" />
<p class="caption">(\#fig:r6)Atalho para abrir e salvar arquivo de dados</p>
</div>

Fonte: Elaborado pelo(s) autor(es)

Outra op��o com mesmo efeito � utilizar o comando a seguir diretamente no console do RStudio: 

`save("nomeDoObjeto",file="nomeDoArquivo.RData")`

O nome do objeto pode ser uma lista de objetos para salvar mais de um objeto do ambiente, `list=("objeto1", "objeto2")`. Para carregar um arquivo RData no ambiente, o comando a ser utilizado pelo usu�rio � 

`load("arquivo.RData")`,

desde que o arquivo esteja no diret�rio de trabalho do R.

� poss�vel exportar as bases trabalhadas para v�rios formatos de arquivos de dados e de texto, como seguem alguns exemplos:

- `write.csv(nomeobjeto,"file.csv", sep=";")`: salvando em arquivo csv.
- `write.foreign(nomeobjeto,"d:/nome.sps")`: arquivos sps.
- `write.foreign(nomeobjeto,"d:/nome.dta")`: arquivos dta.
- `write.foreign(nomeobjeto,"d:/nome.sas7bdat")`: arquivos sas7bdat.

## Diret�rios de trabalho

Os trabalhos efetudados via Rstudio, incluindo as bases de dados, os objetos, os resultados das f�rmulas, os c�lculos aplicados sobre os vetores e demais arquivos resultantes da utiliza��o do programa podem ser salvos em seu diret�rio de arquivos. Ap�s instalado o Rstudio  destina um diret�rio padr�o salvar estes arquivos, o qual pode ser verificado com o comando `getwd()`. 

Este caminho padr�o, por sua vez, pode ser alterado via comando

`setwd("C://file/path")`

onde o usu�rio escolhe a pasta desejada que ficar� como padr�o. O comando `dir()` mostra ao usu�rio os documentos que constam no diret�rio padr�o ou o escolhido para a consulta.

## Opera��es

### Opera��es Aritm�ticas

A realiza��o de uma opera��o aritm�tica no R acontece da seguinte forma: onde a resolu��o das opera��es segue o padr�o, ou seja, primeiro exponencia��es, seguido de multiplica��es e divis�es, deixando por ultimo adi��es e subtra��es, de acordo com a ordem que est�o dispostas. Para alterar a prioridade da resolu��o de opera��es fazemos o uso do parenteses para destacar a opera��o que deve ser priorit�ria na resolu��o. Seguem alguns exemplos efetuados diretamente no console do RStudio:


```r
# soma
19+26
```

```
[1] 45
```

```r
# subtra��o
19-26
```

```
[1] -7
```

```r
# divis�o
4/2
```

```
[1] 2
```

```r
# multiplica��o 
4*2
```

```
[1] 8
```

```r
# exponencia��o
4^2
```

```
[1] 16
```

```r
# prioridade de resolu��o
19 + 26 /4 -2 *10
```

```
[1] 5.5
```

```r
((19 + 26) /(4 -2))*10
```

```
[1] 225
```

```r
# raiz quadrada
sqrt(16)
```

```
[1] 4
```

```r
# Logaritmo 
log(1)
```

```
[1] 0
```

### Opera��es L�gicas

O ambiente de programa��o Rstudio trabalha com algumas opera��es l�gicas, que ser�o importantes na manipula��o de bases de dados:

- $a == b$ ("a" � igual a "b")
- $a != b$ ("a" � diferente a "b")
- $a > b$ ("a" � maior que "b")
- $a < b$ ("a" � menor  que "b")
- $a >= b$ ("a" � maior ou igual a "b")
- $a <= b$ ("a" � menor ou igual a "b")
- is.na ("a" � missing - faltante)
- is.null ("a" � nulo)

Seguem alguns exemplos da aplica��o das opera��es l�gicas:


```r
# maior que 
2 > 1
```

```
[1] TRUE
```

```r
1 > 2
```

```
[1] FALSE
```

```r
# menor que 
1 < 2
```

```
[1] TRUE
```

```r
# maior ou igual a 
0 >= (2+(-2))
```

```
[1] TRUE
```

```r
# menor ou igual a 
1 <= 3
```

```
[1] TRUE
```

```r
# conjun��o
9 > 11 & 0 < 1
```

```
[1] FALSE
```

```r
# ou
6 < 5 | 0 > -1
```

```
[1] TRUE
```

```r
# igual a
1 == 2/2
```

```
[1] TRUE
```

```r
# diferente de
1 != 2
```

```
[1] TRUE
```

## Cria��o de objetos

A linguagem de programa��o R se configura em uma linguagem orientada a objetos, ou seja, a todo tempo estamos criando diversos tipos de objetos e efetuando opera��es com os mesmos. Por exemplo, a cria��o de listas, bases de dados, uni�o de bases de dados, data.frames e at� mesmo mapas!


```r
#Criando um objeto simples
objeto = "meu primeiro objeto" #enter
#Agora para retomar o objeto criado:
objeto #enter
```

```
[1] "meu primeiro objeto"
```

```r
#Pode ser efetuada uma opera��o:
a= 2+1
a
```

```
[1] 3
```

O comando `ls()` lista todos os objetos que est�o criados no ambiente e `rm(x)` remove o objeto indicado (x). Para remover todos os objetos de uma s� vez utiliza-se `rm(list=ls())`.


```r
#Lista objetos do ambiente
ls()
```

```
[1] "a"      "objeto"
```

```r
#Remover um banco de dados
rm(a)
```

**Convers�o de uma vari�vel**

Para a aplica��o de algumas fun��es � importante que cada vari�vel esteja corretamente classificada, o que em alguns casos n�o ocorre durante o reconhecimento autom�tico do R. Precisamos ent�o reconhec�-la como vari�vel texto, num�rica ou fator. Al�m disso, a classe ordered se aplica a vari�veis categ�ricas que podem ser consideradas orden�veis.


```r
idade=c('11', '12', '31')
nomes=c("Elisa", "Priscila", "Carol")
cep=c(98700000,98701000,98702000)
idade= as.numeric(idade)
idade
```

```
[1] 11 12 31
```

```r
cep = as.character(cep)
cep
```

```
[1] "98700000" "98701000" "98702000"
```

## Algumas fun��es e comandos essenciais

A fun��o `head()` mostra as 6 primeiras colunas do arquivo para se ter uma no��o do conte�do. No caso do mesmo ser um data.frame, podemos solicitar o n�mero de valores ou linhas a serem mostrados no console atrav�s do par�metro n ou na aus�ncia deste, todas as linhas ser�o impressas, como exemplo `head(x ,n=2)` para ver as duas primeiras linhas. 

O comando `summary()` efetua o resumo dos dados, se for qualitativa mostra a frequ�ncia absoluta das categorias e se for quantitativa apresenta as categorias. No exemplo abaixo trabalharemos com uma base de dados de treinamento denominada "iris" que est� acess�vel no *software* RStudio atrav�s do comando que carrega dados espec�ficos `data()`:


```r
#Carregando dados da base do RSdudio iris.
data(iris)

#Visualizando as primeiras 6 colunas
head(iris)
```

```
  Sepal.Length Sepal.Width Petal.Length Petal.Width Species
1          5.1         3.5          1.4         0.2  setosa
2          4.9         3.0          1.4         0.2  setosa
3          4.7         3.2          1.3         0.2  setosa
4          4.6         3.1          1.5         0.2  setosa
5          5.0         3.6          1.4         0.2  setosa
6          5.4         3.9          1.7         0.4  setosa
```

```r
#Resumo do objeto
summary(iris)
```

```
  Sepal.Length   Sepal.Width    Petal.Length   Petal.Width        Species  
 Min.   :4.30   Min.   :2.00   Min.   :1.00   Min.   :0.1   setosa    :50  
 1st Qu.:5.10   1st Qu.:2.80   1st Qu.:1.60   1st Qu.:0.3   versicolor:50  
 Median :5.80   Median :3.00   Median :4.35   Median :1.3   virginica :50  
 Mean   :5.84   Mean   :3.06   Mean   :3.76   Mean   :1.2                  
 3rd Qu.:6.40   3rd Qu.:3.30   3rd Qu.:5.10   3rd Qu.:1.8                  
 Max.   :7.90   Max.   :4.40   Max.   :6.90   Max.   :2.5                  
```

O comando `names()` lista os nomes das colunas dos bancos de dados escolhidos, enquanto `tail()` mostra as �ltimas seis linhas.


```r
#Para visualizar os nomes das colunas dos dados:
names(iris)
```

```
[1] "Sepal.Length" "Sepal.Width"  "Petal.Length" "Petal.Width"  "Species"     
```

```r
#vizualizar as ultimas seis linhas do objetos
tail(iris)
```

```
    Sepal.Length Sepal.Width Petal.Length Petal.Width   Species
145          6.7         3.3          5.7         2.5 virginica
146          6.7         3.0          5.2         2.3 virginica
147          6.3         2.5          5.0         1.9 virginica
148          6.5         3.0          5.2         2.0 virginica
149          6.2         3.4          5.4         2.3 virginica
150          5.9         3.0          5.1         1.8 virginica
```

Para que o pesquisador conhe�a melhor as bases de dados em que est� atuando, o comando `class()` serve para identificar o tipo de base ou dados da base. Com o exemplo abaixo constata-se que o objeto "iris" � um *data frame*, a vari�vel "Sepal.Length" � uma vari�vel num�rica e que a vari�vel num�rica.


```r
class(iris)
```

```
[1] "data.frame"
```

```r
class(iris$Sepal.Length)
```

```
[1] "numeric"
```

```r
class(iris$Especie)
```

```
[1] "NULL"
```

Efeito semelhante possui o comando `ls.str()`:


```r
ls.str(iris)
```

```
Petal.Length :  num [1:150] 1.4 1.4 1.3 1.5 1.4 1.7 1.4 1.5 1.4 1.5 ...
Petal.Width :  num [1:150] 0.2 0.2 0.2 0.2 0.2 0.4 0.3 0.2 0.2 0.1 ...
Sepal.Length :  num [1:150] 5.1 4.9 4.7 4.6 5 5.4 4.6 5 4.4 4.9 ...
Sepal.Width :  num [1:150] 3.5 3 3.2 3.1 3.6 3.9 3.4 3.4 2.9 3.1 ...
Species :  Factor w/ 3 levels "setosa","versicolor",..: 1 1 1 1 1 1 1 1 1 1 ...
```

Os comandos `ncol()` e `nrow()` mostram o n�mero de colunas e o n�mero de linhas do objeto, respectivamente.

### Fun��es *View* e *dim*

A fun��o `View()` permite vizualizar os elementos no script do dataframe requesitado, enquando a fun��o `dim()` (abreviatura de dimens�es) fornece o n�mero de linhas e de colunas, respectivamente.


```r
View(iris)
dim(iris)
```

```
[1] 150   5
```

Para alterar um nome de uma vari�vel pode ser utilizado o comando colnames. No exemplo acima, vamos alterar o nome da coluna "Species" para "Especie". 


```r
#Alterar o nome da coluna, sendo que o '[5]' indica que est� na quinta coluna.
colnames(iris)[5]='Especie'
```

Para selecionarmos uma coluna do objeto "iris", por exemplo a coluna "Sepal.Length", poder�amos digitar no console o comando **iris\$Sepal.Length**. O padr�o de carregamento da base de dados nos obriga a dizer ao R qual � a base que quer selecionar (iris), inserindo o s�mbolo `$` e ap�s o nome da coluna a qual deseja as informa��es. Para criar um novo objeto com esta informa��o, basta dizer ao R, como j� visto acima, por exemplo: **novoobjeto=iris\$novacoluna**.

No entanto, para acessar os dados sem o uso do s�mbolo `$`, podemos usar o seguinte comando: **attach(iris)**. Assim, podemos efetuar o sum�rio da coluna "Petal.Width":


```r
#Definindo a fun��o attach para o objeto 'dados'.
attach(iris)
#Efetuando o sum�rio de 'pop.total'.
summary(Petal.Width)
```

```
   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    0.1     0.3     1.3     1.2     1.8     2.5 
```

```r
#Como a coluna 'distrito' � um fator, o sum�rio ser� 
#a contagem da quantidade de cada fator na coluna.
summary(Especie)
```

```
    setosa versicolor  virginica 
        50         50         50 
```


### Fun��o *tapply*

O comando `tapply()` agrega os dados pelos n�veis das vari�veis qualitativas. Note que a coluna "Especie" possui dados em forma de fatores. Assim, para filtrarmos a informa��o (coluna "Sepal.Length") m�dia por Especie, podemos utilizar:


```r
#Fun��o 'tapply', n�mero m�dio da popula��o total por distrito.
tapply(Sepal.Length, Especie, mean)
```

```
    setosa versicolor  virginica 
     5.006      5.936      6.588 
```

No caso da coluna "Sepal.Length", se ela possuir um registro NA (faltante), para que se efetue a m�dia por este coluna neste quesito, h� que se adicionar o par�metro `na.rm=T`, que ignora as c�lulas faltantes para calcular-se a m�dia:


```r
#Fun��o 'tapply' considerando NAs:
tapply(Sepal.Length, Especie, mean)
```

```
    setosa versicolor  virginica 
     5.006      5.936      6.588 
```

```r
#Fun��o 'tapply' sem considerar NAs:
tapply(Sepal.Length, Especie, mean, na.rm=T)
```

```
    setosa versicolor  virginica 
     5.006      5.936      6.588 
```

### Fun��o *subset*

Utiliza-se o comando `subset()` para formar um subconjunto de dados o qual desejamos selecionar de um objeto. Por exemplo, se quisermos criar um novo objeto com somente os dados da "Especie" setosa:


```r
dadossetosa=subset(iris, Especie=='setosa')
head(dadossetosa)
```

```
  Sepal.Length Sepal.Width Petal.Length Petal.Width Especie
1          5.1         3.5          1.4         0.2  setosa
2          4.9         3.0          1.4         0.2  setosa
3          4.7         3.2          1.3         0.2  setosa
4          4.6         3.1          1.5         0.2  setosa
5          5.0         3.6          1.4         0.2  setosa
6          5.4         3.9          1.7         0.4  setosa
```

Pode ser configurado mais de uma condi��o para a filtragem dos dados, por exemplo, al�m de serem filtrados os dados referentes a Especie setosa, aquelas na qual o Sepal.Length � superior a 5. Como no exemplo, criamos um novo objeto com estas condi��es:


```r
dadossetosa2=subset(iris, Especie=='setosa'& Sepal.Length>5)
head(dadossetosa2)
```

```
   Sepal.Length Sepal.Width Petal.Length Petal.Width Especie
1           5.1         3.5          1.4         0.2  setosa
6           5.4         3.9          1.7         0.4  setosa
11          5.4         3.7          1.5         0.2  setosa
15          5.8         4.0          1.2         0.2  setosa
16          5.7         4.4          1.5         0.4  setosa
17          5.4         3.9          1.3         0.4  setosa
```

### Fun��o *table*

Para contar elementos em cada n�vel de um fator, usa-se a fun��o `table()`. A fun��o pode fazer tabula��es cruzadas, gerando uma tabela de conting�ncia, esse tipo de tabela � usado para registrar observa��es independentes de duas ou mais vari�veis aleat�rias.

Para exemplo da utiliza��o da fun��o `table` agora com dados qualitativos (g�nero e sa�de), vamos utilizar a base de dados `cdc`:


```r
# Carregando a base
source("http://www.openintro.org/stat/data/cdc.R")
#Vizualizamos as primeiras linhas
head(cdc)
```

```
    genhlth exerany hlthplan smoke100 height weight wtdesire age gender
1      good       0        1        0     70    175      175  77      m
2      good       0        1        1     64    125      115  33      f
3      good       1        1        1     60    105      105  49      f
4      good       1        1        0     66    132      124  42      f
5 very good       0        1        0     61    150      130  55      f
6 very good       1        1        0     64    114      114  55      f
```

```r
# Efetuamos a contagem dos dados qualitativos com a fun��o table
table(cdc$genhlth,cdc$gender)
```

```
           
               m    f
  excellent 2298 2359
  very good 3382 3590
  good      2722 2953
  fair       884 1135
  poor       283  394
```


## Estrutura de dados

### Vetores

Os fatores s�o uma classe especial de vetores, que definem vari�veis categ�ricas de classifica��o, como os tratamentos em um experimento fatorial, ou categorias em uma tabela de conting�ncia.


```r
# Cria��o de um vetor
c(2, 4, 6)
```

```
[1] 2 4 6
```

Os vetores podem ser criados a partir de uma sequ�ncia num�rica ou mesmo de um intervalo entre valores:


```r
c(2:6)
```

```
[1] 2 3 4 5 6
```

```r
# Cria��o de um vetor a partir do intervalo entre cada elemento e valores
#m�nimo e m�ximo
seq(2, 3, by=0.5)
```

```
[1] 2.0 2.5 3.0
```

Cria��o de um vetor atr�ves de uma repeti��o tamb�m � �til em v�rias situa��es. No primeiro exemplo repete o intervalo de 1 a 3 4 vezes e no segundo exemplo, a cada 3 vezes:


```r
rep(1:3, times=4)
```

```
 [1] 1 2 3 1 2 3 1 2 3 1 2 3
```

```r
rep(1:3, each=3)
```

```
[1] 1 1 1 2 2 2 3 3 3
```

A fun��o factor cria um fator, a partir de um vetor:


```r
sexo<-factor(rep(c("F", "M"),each=8))
sexo
```

```
 [1] F F F F F F F F M M M M M M M M
Levels: F M
```

```r
numeros=rep(1:3,each=3)
numeros
```

```
[1] 1 1 1 2 2 2 3 3 3
```

```r
numeros.f<-factor(numeros)
numeros.f
```

```
[1] 1 1 1 2 2 2 3 3 3
Levels: 1 2 3
```


Fatores t�m um atributo que especifica seus n�veis ou categorias (levels), que seguem ordem alfanum�rica crescente, por *default*. Em muitas an�lises essa ordem � de fundamental import�ncia e dessa forma pode ser alterada atrav�s do argumento levels, por exemplo, para que possa ser colocado o controle antes dos tratamentos: 


```r
tratamentos=factor(rep(c("controle","adubo A","adubo B"), each=4))
tratamentos
```

```
 [1] controle controle controle controle adubo A  adubo A  adubo A  adubo A 
 [9] adubo B  adubo B  adubo B  adubo B 
Levels: adubo A adubo B controle
```

```r
tratamentos=factor(rep(c("controle","adubo A","adubo B"), each=4), 
levels=c("controle", "adubo A", "adubo B"))
tratamentos
```

```
 [1] controle controle controle controle adubo A  adubo A  adubo A  adubo A 
 [9] adubo B  adubo B  adubo B  adubo B 
Levels: controle adubo A adubo B
```

Fatores podem conter n�veis n�o usados (vazios):


```r
participantes=factor(rep("mulheres",10), levels=c("mulheres","homens"))
participantes
```

```
 [1] mulheres mulheres mulheres mulheres mulheres mulheres mulheres mulheres
 [9] mulheres mulheres
Levels: mulheres homens
```
<!--
Tamb�m � poss�vel aplicar uma fun��o aos subconjuntos de um vetor definidos por um fator utilizando a fun��o `tapply()`. Criamos um objeto com o sexo das pessoas, seguido pela dieta e peso (que caracterizamos como num�rico). Depois, determinamos a m�dia de peso frente ao sexo e a dieta


```r
sexo=factor(rep(c("F","M"),each=9))
dieta=factor(rep(rep(c("normal","light","diet"), each=3),2), 
levels=c("normal", "light","diet"))
peso=c(90, 89, 78, 69, 85, 69, 77, 89, 80, 60, 75, 79, 65, 94,
       69, 85, 69, 77)
sexo
```

```
 [1] F F F F F F F F F M M M M M M M M M
Levels: F M
```

```r
dieta
```

```
 [1] normal normal normal light  light  light  diet   diet   diet   normal
[11] normal normal light  light  light  diet   diet   diet  
Levels: normal light diet
```

```r
peso=as.numeric(peso)

# m�dia de peso frente ao sexo e dieta
tapply(peso,list(sexo,dieta), mean)
```

```
  normal light diet
F  85.67 74.33   82
M  71.33 76.00   77
```
-->


### Matrizes

A fun��o matrix tem a finalidade de criar uma matriz com os valores do argumento data, argumento este que insere as vari�veis desejadas na matriz. O n�mero de linhas � definido pelo argumento nrow e o n�mero de colunas � definido pelo argumento ncol: 


```r
nome.da.matriz= matrix(data=1:12,nrow = 3,ncol = 4)
nome.da.matriz
```

```
     [,1] [,2] [,3] [,4]
[1,]    1    4    7   10
[2,]    2    5    8   11
[3,]    3    6    9   12
```


Por *default* (a��o tomada pelo *software*), os valores s�o preenchidos por coluna. Para preencher por linha basta instruir o programa de outra forma, alterando o argumento `byrow` para TRUE:


```r
nome.da.matriz= matrix(data=1:12,nrow = 3,ncol = 4, byrow=T)
nome.da.matriz
```

```
     [,1] [,2] [,3] [,4]
[1,]    1    2    3    4
[2,]    5    6    7    8
[3,]    9   10   11   12
```

Se a matriz inserida tem menos elementos do que a ordem informada para a matriz, os s�o repetidos at� preench�-la:


```r
lista= list(matriz=matrix(c(1,2,1), nrow=3, ncol=2))
lista
```

```
$matriz
     [,1] [,2]
[1,]    1    1
[2,]    2    2
[3,]    1    1
```

### Listas

As listas podem ser criadas a partir do comando `list()`. 

- **nrow**: corresponde ao n�mero de linhas;
- **ncol**: corresponde ao n�mero de colunas.

Para ver quais elementos est�o em suas listas � s� chamar pelo nome que foi dado para ela, como no exemplo abaixo. Representa uma cole��o de objetos.


```r
lista= list(matriz=matrix(c(1,2,1,5,7,9), nrow=3, ncol=2),vetor=1:6)
lista
```

```
$matriz
     [,1] [,2]
[1,]    1    5
[2,]    2    7
[3,]    1    9

$vetor
[1] 1 2 3 4 5 6
```

**Comandos para manipula��o de listas**

Para descobrirmos de maneira r�pida o n�meros de objetos que h� na lista, utilizamos o comando `length(nomedalista)`.


```r
lista
```

```
$matriz
     [,1] [,2]
[1,]    1    5
[2,]    2    7
[3,]    1    9

$vetor
[1] 1 2 3 4 5 6
```

```r
length(lista)
```

```
[1] 2
```

O uso do comando `names(nomedalista)` retorna os nomes dos objetos que est�o presentes na lista.


```r
names(lista)
```

```
[1] "matriz" "vetor" 
```

Para chamar v�rias listas atrav�s usamos o comando da seguinte forma:

`c(nome1, nome2)`


```r
lista.1= list(matriz=matrix(c(1,2,1,5,7,9), nrow=3, ncol=2),
              vetor=1:6)
lista.2= list(nomes=c("Marcelo", "F�bio", "Felipe"), 
              idade=c(25, 34, 26))
c(lista.1,lista.2)
```

```
$matriz
     [,1] [,2]
[1,]    1    5
[2,]    2    7
[3,]    1    9

$vetor
[1] 1 2 3 4 5 6

$nomes
[1] "Marcelo" "F�bio"   "Felipe" 

$idade
[1] 25 34 26
```

### Data frames

Com a fun��o `data.frame()` reunimos vetores de mesmo comprimento em um s� objeto. Neste caso s�o criadas tabelas de dados. Cada observa��o � descrita por um conjunto de propriedades. Abaixo podemos ver como inserir os dados para criar a "tabela". Similar como matrizes, porem diferentes colunas podem possuir elementos de natureza diferentes .


```r
estudantes= c("Camila", "Pedro", "Marcelo","Guilherme")
idade=c(21,17,17,18)
peso=c(65,79,80,100)
informacoes=data.frame(estudantes,idade,peso)
informacoes
```

```
  estudantes idade peso
1     Camila    21   65
2      Pedro    17   79
3    Marcelo    17   80
4  Guilherme    18  100
```

Adiciona-se colunas no *data frame* atrav�s do comando a seguir, pressupondo que a ordem dos dados esteja correta:

`nomedodata.frame$vari�velaseradicionada`


```r
informacoes$cidades=c("Nova Hartz","Gramado","Soledade",
                      "Porto Alegre")
informacoes
```

```
  estudantes idade peso      cidades
1     Camila    21   65   Nova Hartz
2      Pedro    17   79      Gramado
3    Marcelo    17   80     Soledade
4  Guilherme    18  100 Porto Alegre
```

� poss�vel fazer uma contagem concatenando com a filtragem do pacote `subset`, como no exemplo a contagem dos indiv�duos cuja origem � Soledade.


```r
length(subset(informacoes$cidades, informacoes$cidades=="Soledade"))
```

```
[1] 1
```

## Manipula��o de banco de dados

<!--
## Fun��es
-->

A fun��o `edit()` abre uma interface simples de edi��o de dados em formato planilha, e � �til para pequenas modifica��es. Mas para salvar as modifica��es atribua o resultado da fun��o `edit` a um objeto.

Utiliza-se o comando da seguinte forma: 


`novonomedabase = edit(nomeatualdabase)`


```r
informacoes.2=edit(informacoes)
```

<div class="figure" style="text-align: center">
<img src="95.png" alt="Editor de dados" width="80%" />
<p class="caption">(\#fig:95)Editor de dados</p>
</div>

Basta clicar no ret�ngulo correspondente a vari�vel que deseja ser modificada, excluir ou adicionar novas colunas.

<div class="figure" style="text-align: center">
<img src="10.png" alt="Acr�scimo de uma nova coluna atrav�s do editor de dados" width="80%" />
<p class="caption">(\#fig:10)Acr�scimo de uma nova coluna atrav�s do editor de dados</p>
</div>

Logo, chamando o novo banco de dados, teremos:


```r
informacoes.2 
```

```
  estudantes idade peso      cidades
1     Camila    21   65   Nova Hartz
2      Pedro    17   79      Gramado
3    Marcelo    17   80     Soledade
4  Guilherme    18  100 Porto Alegre
```


As fun��es a seguir s�o aplic�veis a vetores, data.frames e listas, e em muitos casos trazem praticidade a uma an�lise estat�stica. Foram criados objetos com informa��es do nome dos estudantes e altura. Segue o processo de cria��o do *data frame* com estas informa��es, lembrando que esta forma de "uni�o" das informa��es pressup�e que a ordem dos dados esteja correta:


```r
# Cri��o do data frame
estudantes=c("Guilherme", "Marcelo", "Pedro", "Camila")
altura= c(1.50, 1.9, 1.74, 1.80)
informacoes.3=data.frame(estudantes, altura)
```

J� o comando `merge()` serve para juntar dois *data frames* que possuam uma coluna em comum. Neste caso, unimos o objeto `informa��es.2` com o objeto `informa��es.3` utilizando o nome dos estudantes (informa��o em comum):


```r
# Uni�o de um banco de dados (existencia de uma v�riavel em comum)

informacoes=merge(informacoes.2,informacoes.3, by="estudantes")
```

Adicionar um c�lculo entre as colunas � muito simples com o RStudio, neste caso com os dados do peso e altura, pode-se calcular o IMC (�ndice de Massa Corporal) em uma nova coluna:


```r
informacoes$Imc=c(informacoes$peso/(informacoes$altura^2))
informacoes
```

```
  estudantes idade peso      cidades altura   Imc
1     Camila    21   65   Nova Hartz   1.80 20.06
2  Guilherme    18  100 Porto Alegre   1.50 44.44
3    Marcelo    17   80     Soledade   1.90 22.16
4      Pedro    17   79      Gramado   1.74 26.09
```

Ainda, se houver linhas que tenham pelo menos uma informa��o faltante (NA), estas podem ser exclu�das com o comando `na.omit()`, ou mesmo os NAs serem substitu�dos por outro caractere (neste caso foi substitu�do por zero) com o comando `is.na`:


```r
# Retirar as linhas que tenham pelo menos um NA:

informacoes<- na.omit(informacoes)
informacoes
```

```
  estudantes idade peso      cidades altura   Imc
1     Camila    21   65   Nova Hartz   1.80 20.06
2  Guilherme    18  100 Porto Alegre   1.50 44.44
3    Marcelo    17   80     Soledade   1.90 22.16
4      Pedro    17   79      Gramado   1.74 26.09
```

```r
# Substituir NA's por zero no data.frame

informacoes[is.na(informacoes)] = 0
informacoes
```

```
  estudantes idade peso      cidades altura   Imc
1     Camila    21   65   Nova Hartz   1.80 20.06
2  Guilherme    18  100 Porto Alegre   1.50 44.44
3    Marcelo    17   80     Soledade   1.90 22.16
4      Pedro    17   79      Gramado   1.74 26.09
```

Outro recurso interessante � a substitui��o de dados em uma coluna, que pode ser feito de forma autom�tica para uma condi��o padr�o escolhida. No exemplo abaixo, substituimos aquelas informa��es de idade igual a 17 pelo n�mero 19:


```r
# Substituir n�meros na coluna
informacoes$idade[informacoes$idade == 17] <- 19
informacoes
```

```
  estudantes idade peso      cidades altura   Imc
1     Camila    21   65   Nova Hartz   1.80 20.06
2  Guilherme    18  100 Porto Alegre   1.50 44.44
3    Marcelo    19   80     Soledade   1.90 22.16
4      Pedro    19   79      Gramado   1.74 26.09
```

A classifica��o qualitativa das informa��es, com base em condi��es definidas pelo usu�rio podem ser facilmente efetuadas pelo comando `ifelse`. Para quem n�o tem intimidade com atributos de programa��o, este comando seleciona "se" (*if*) uma informa��o desejada � atendida, e cria uma rotina (*else*) que ser� aplicada "ent�o". 

No nosso exemplo, cria-se um objeto "classificacao" e se a coluna IMC conter dados acima de 25, ser� marcado como "peso normal", sendo que do contr�rio, constar� como "excesso de peso". Ap�s utilizamos o comando `cbind()` para unir os dois objetos pelas colunas. caso n�o queira utilizar o comando `cbind()`, poderia ser criado uma nova coluna com o nome do obetjo sendo "informacoes\$classificacao".


```r
# Classificar qualitativamente informa��es em um determinado intervalo 
classificacao=ifelse(informacoes$Imc<25, "peso normal", 
                     "excesso de peso")
informacoes=cbind(informacoes, classificacao)
informacoes
```

```
  estudantes idade peso      cidades altura   Imc   classificacao
1     Camila    21   65   Nova Hartz   1.80 20.06     peso normal
2  Guilherme    18  100 Porto Alegre   1.50 44.44 excesso de peso
3    Marcelo    19   80     Soledade   1.90 22.16     peso normal
4      Pedro    19   79      Gramado   1.74 26.09 excesso de peso
```


Table: (\#tab:imct)Valores padr�o para o IMC

Resultado            Significado             
-------------------  ------------------------
Abaixo de 17         Muito abaixo do peso    
Entre 17 e 18,49     Abaixo do peso          
Entre 18,5 e 24,99   Peso normal             
Entre 25 e 29,99     Acima do peso           
Entre 30 e 34,99     Obesidade I             
Entre 35 e 39,99     Obesidade II (severa)   
Acima de 40          Obesidade III (m�rbida) 

No entanto, o IMC possui v�rias classifica��es de acordo com o seu resultado (Tabela \@ref(tab:imct)), sendo que, por exemplo, resultados abaixo de 17 informam que o indiv�duo se encontra como Muito abaixo do peso, e acima de 40, se encontra em Obesidade III. Para efetuar a classifica��o desta maneira utilizando o comando `ifelse`, ou seja, com mais de uma condi��o, pode ser efetuada a estrutura��o com a aglutina��o do comando:


```r
informacoes$tipoimc=ifelse(informacoes$Imc<17, "Muito abaixo do peso",
ifelse(informacoes$Imc>=17&informacoes$Imc<=18.49,"Abaixo do peso",
ifelse(informacoes$Imc>=18.5&informacoes$Imc<=24.99,"Peso Normal",
ifelse(informacoes$Imc>=25&informacoes$Imc<=29.99,"Acima do Peso",
ifelse(informacoes$Imc>=30&informacoes$Imc<=34.99,"Obesidade I",
ifelse(informacoes$Imc>=35&informacoes$Imc<=39.99,"Obesidade II",
       "Obesidade III"))))))
informacoes
```

```
  estudantes idade peso      cidades altura   Imc   classificacao       tipoimc
1     Camila    21   65   Nova Hartz   1.80 20.06     peso normal   Peso Normal
2  Guilherme    18  100 Porto Alegre   1.50 44.44 excesso de peso Obesidade III
3    Marcelo    19   80     Soledade   1.90 22.16     peso normal   Peso Normal
4      Pedro    19   79      Gramado   1.74 26.09 excesso de peso Acima do Peso
```

A classifica��o bin�ria dos dados (0,1) tamb�m � relevante para o estudo da manipula��o dos dados trabalhados pelo pesquisador. Neste exemplo, classificou-se aqueles valores da coluna "classificacao" com o "peso normal" iguais a 1, do contr�rio classificou-se 0 (zero).


```r
# Classificar informa��es usando o c�digo bin�rio
informacoes$binario= ifelse(informacoes$classificacao 
                            == 'peso normal', 1, 0) 
informacoes
```

```
  estudantes idade peso      cidades altura   Imc   classificacao       tipoimc
1     Camila    21   65   Nova Hartz   1.80 20.06     peso normal   Peso Normal
2  Guilherme    18  100 Porto Alegre   1.50 44.44 excesso de peso Obesidade III
3    Marcelo    19   80     Soledade   1.90 22.16     peso normal   Peso Normal
4      Pedro    19   79      Gramado   1.74 26.09 excesso de peso Acima do Peso
  binario
1       1
2       0
3       1
4       0
```

O comando `rbind()` � utilizado para incluir linhas novas abaixo de um objeto j� criado pelo pesquisador, sendo que � importante o cuidado de que estas novas informa��es tenham os mesmos campos (colunas). A exemplo, pede-se para incluir uma nova pessoa no *data frame* informacoes: Francisco, 30 anos de idade, peso 59, natural de Iju�, IMC 23,33768, classificado como peso normal. Lembrando de incluir os campos "tipoimc" e "binario".


```r
novo1=data.frame(estudantes="Francisco", idade=30, peso=59, 
                 cidades="Iju�", 
                 altura="1,59", 
                 Imc= 23.33768, 
                 classificacao= "peso normal",
                 tipoimc="Peso Normal", 
                 binario=1)
informacoes=rbind(informacoes, novo1)
informacoes
```

```
  estudantes idade peso      cidades altura   Imc   classificacao       tipoimc
1     Camila    21   65   Nova Hartz    1.8 20.06     peso normal   Peso Normal
2  Guilherme    18  100 Porto Alegre    1.5 44.44 excesso de peso Obesidade III
3    Marcelo    19   80     Soledade    1.9 22.16     peso normal   Peso Normal
4      Pedro    19   79      Gramado   1.74 26.09 excesso de peso Acima do Peso
5  Francisco    30   59         Iju�   1,59 23.34     peso normal   Peso Normal
  binario
1       1
2       0
3       1
4       0
5       1
```

Outra forma de incluir informa��es adicionais nos *data frames* atrav�s de atributos � utilizando o pacote `dplyr`. Decide-se criar um campo "faixa et�ria", sendo que aqueles indiv�duos com idade acima de 21 chamaremos de "adulto" e do contr�rio "n�o adulto".


```r
require(dplyr)
```

```
Carregando pacotes exigidos: dplyr
```

```

Attaching package: 'dplyr'
```

```
The following objects are masked from 'package:stats':

    filter, lag
```

```
The following objects are masked from 'package:base':

    intersect, setdiff, setequal, union
```

```r
informacoes= mutate(informacoes, 
                    "faixa etaria"= ifelse(informacoes$idade<21,
                                           "n�o adulto", "adulto"))
informacoes
```

```
  estudantes idade peso      cidades altura   Imc   classificacao       tipoimc
1     Camila    21   65   Nova Hartz    1.8 20.06     peso normal   Peso Normal
2  Guilherme    18  100 Porto Alegre    1.5 44.44 excesso de peso Obesidade III
3    Marcelo    19   80     Soledade    1.9 22.16     peso normal   Peso Normal
4      Pedro    19   79      Gramado   1.74 26.09 excesso de peso Acima do Peso
5  Francisco    30   59         Iju�   1,59 23.34     peso normal   Peso Normal
  binario faixa etaria
1       1       adulto
2       0   n�o adulto
3       1   n�o adulto
4       0   n�o adulto
5       1       adulto
```

A (re)ordena��o das colunas de um *data frame* pode ser muito �til em alguns casos, sendo extremamente f�cil efetu�-la, cada n�mero representa o n�mero da respectiva coluna:


```r
# Reordenar colunas
informacoes=informacoes[c(8,2,3,4,1,6,5,7,9,10)]
```

Caso se queira a invers�o total da ordem das colunas do objeto estudado, o comando `rev()` pode ser �til:


```r
# Invers�o do posicionamento dos elementos
rev(informacoes)
```

```
  faixa etaria binario   classificacao altura   Imc estudantes      cidades
1       adulto       1     peso normal    1.8 20.06     Camila   Nova Hartz
2   n�o adulto       0 excesso de peso    1.5 44.44  Guilherme Porto Alegre
3   n�o adulto       1     peso normal    1.9 22.16    Marcelo     Soledade
4   n�o adulto       0 excesso de peso   1.74 26.09      Pedro      Gramado
5       adulto       1     peso normal   1,59 23.34  Francisco         Iju�
  peso idade       tipoimc
1   65    21   Peso Normal
2  100    18 Obesidade III
3   80    19   Peso Normal
4   79    19 Acima do Peso
5   59    30   Peso Normal
```

A  fun��o `table()` faz a contagem os dados; j� o comando `sort()` ordena os objetos em ordem crescente (caso queira no formato decrescente, informar `decreasing=TRUE`).


```r
# contagem de objetos
table(informacoes$classificacao)
```

```

excesso de peso     peso normal 
              2               3 
```

```r
# Ordenar os objetos em ordem crescente
sort(informacoes$idade)
```

```
[1] 18 19 19 21 30
```

A ordena��o de todo o *data frame* a partir de uma vari�vel, pode ser realizada utilizando o comando `order`, sendo que pode ser realizada inclusive com vari�veis categ�ricas (no exemplo abaixo o nome das cidades).


```r
# Ordem decrescente 
informacoes[order(informacoes$idade, decreasing = TRUE),]
```

```
        tipoimc idade peso      cidades estudantes   Imc altura   classificacao
5   Peso Normal    30   59         Iju�  Francisco 23.34   1,59     peso normal
1   Peso Normal    21   65   Nova Hartz     Camila 20.06    1.8     peso normal
3   Peso Normal    19   80     Soledade    Marcelo 22.16    1.9     peso normal
4 Acima do Peso    19   79      Gramado      Pedro 26.09   1.74 excesso de peso
2 Obesidade III    18  100 Porto Alegre  Guilherme 44.44    1.5 excesso de peso
  binario faixa etaria
5       1       adulto
1       1       adulto
3       1   n�o adulto
4       0   n�o adulto
2       0   n�o adulto
```

```r
#ordem crescente
informacoes[order(informacoes$idade, decreasing = FALSE),]
```

```
        tipoimc idade peso      cidades estudantes   Imc altura   classificacao
2 Obesidade III    18  100 Porto Alegre  Guilherme 44.44    1.5 excesso de peso
3   Peso Normal    19   80     Soledade    Marcelo 22.16    1.9     peso normal
4 Acima do Peso    19   79      Gramado      Pedro 26.09   1.74 excesso de peso
1   Peso Normal    21   65   Nova Hartz     Camila 20.06    1.8     peso normal
5   Peso Normal    30   59         Iju�  Francisco 23.34   1,59     peso normal
  binario faixa etaria
2       0   n�o adulto
3       1   n�o adulto
4       0   n�o adulto
1       1       adulto
5       1       adulto
```

```r
#ordem crescente
informacoes[order(informacoes$cidades, decreasing = FALSE),]
```

```
        tipoimc idade peso      cidades estudantes   Imc altura   classificacao
4 Acima do Peso    19   79      Gramado      Pedro 26.09   1.74 excesso de peso
5   Peso Normal    30   59         Iju�  Francisco 23.34   1,59     peso normal
1   Peso Normal    21   65   Nova Hartz     Camila 20.06    1.8     peso normal
2 Obesidade III    18  100 Porto Alegre  Guilherme 44.44    1.5 excesso de peso
3   Peso Normal    19   80     Soledade    Marcelo 22.16    1.9     peso normal
  binario faixa etaria
4       0   n�o adulto
5       1       adulto
1       1       adulto
2       0   n�o adulto
3       1   n�o adulto
```

O comando `rank()` cria uma ranqueamento crescente das informa��es. Se pretende-se, por exemplo, criar uma coluna com o ranking dos valores do IMC, pode ser utilizado:


```r
informacoes$rankingImc=rank(informacoes$Imc)
informacoes
```

```
        tipoimc idade peso      cidades estudantes   Imc altura   classificacao
1   Peso Normal    21   65   Nova Hartz     Camila 20.06    1.8     peso normal
2 Obesidade III    18  100 Porto Alegre  Guilherme 44.44    1.5 excesso de peso
3   Peso Normal    19   80     Soledade    Marcelo 22.16    1.9     peso normal
4 Acima do Peso    19   79      Gramado      Pedro 26.09   1.74 excesso de peso
5   Peso Normal    30   59         Iju�  Francisco 23.34   1,59     peso normal
  binario faixa etaria rankingImc
1       1       adulto          1
2       0   n�o adulto          5
3       1   n�o adulto          2
4       0   n�o adulto          4
5       1       adulto          3
```

Para utilizar a fun��o `rank` com os maiores valores em primeiro lugar:


```r
rank(-informacoes$Imc)
```

```
[1] 5 1 4 2 3
```


## Fun��es Matem�ticas

A utiliza��o de fun��es matem�ticasno RStudio contribui para que o pesquisador possa realizar v�rios experimentos com seus dados. Os c�lculos podem ser efetuados diretamente no console do programa ou aplicados aos objetos criados:


```r
log(1.5)
```

```
[1] 0.4055
```

```r
exp(1)
```

```
[1] 2.718
```

No caso do *data frame* o qual foi criado acima ("informacoes"), pode-se buscar as informa��es dos valores m�nimos (fun��o `min()`), m�ximos (`max()`) da base:


```r
max(informacoes$idade)
```

```
[1] 30
```

```r
min(informacoes$idade)
```

```
[1] 18
```

Ainda, se o interesse est� em descobrir a posi��o, no *data frame}, do peso m�nimo e m�ximo da amostra utiliza-se o comando `which.min` e `which.max`.


```r
# Para descobrir em qual posi��o se encontra o peso m�nimo:
which.min(informacoes$peso)
```

```
[1] 5
```

```r
which.max(informacoes$peso)
```

```
[1] 2
```

Para descobrir qual � o estutande que possui o peso m�nimo, por exemplo, ou o Imc m�ximo, utiliza-se o seguinte comando (notem que os resultados trazem a lista de todos os estudantes comparados):


```r
informacoes$estudantes[which.min(informacoes$peso)]
```

```
[1] Francisco
Levels: Camila Guilherme Marcelo Pedro Francisco
```

```r
informacoes$estudantes[which.max(informacoes$Imc)]
```

```
[1] Guilherme
Levels: Camila Guilherme Marcelo Pedro Francisco
```

O arredondamento de valores num�ricos pode ser feito utilizando o comando `round()`, o qual o pesquisador informa o n�mero de casas decimais:


```r
# Arredondar para n casas decimais
round(informacoes$Imc, 2)
```

```
[1] 20.06 44.44 22.16 26.09 23.34
```

J� o comando `signif()` determina o n�mero de algarismos significativos da s�rie escolhida, ou seja, ele arredonda para os valores em seu primeiro argumento com os n�mero de d�gitos detemrinados: 


```r
x2 <- pi * 100^(-1:3)
round(x2, 3)
```

```
[1] 3.100e-02 3.142e+00 3.142e+02 3.142e+04 3.142e+06
```

```r
signif(x2, 3) 
```

```
[1] 3.14e-02 3.14e+00 3.14e+02 3.14e+04 3.14e+06
```

A soma do total da coluna idade, o desvio padr�o, a vari�ncia, a m�dia aritm�tica e mediana podem ser encontrados, respectivamente, pelos comandos `sum()`, `sd()`, `var()`, `mean()`, `median()`:


```r
# Realiza a somat�ria dos valores
sum(informacoes$idade)
```

```
[1] 107
```

```r
# Desvio padr�o
sd(informacoes$idade)
```

```
[1] 4.93
```

```r
# Variancia
var(informacoes$idade)
```

```
[1] 24.3
```

```r
# Calcula a m�dia aritm�tica dos valores
mean(informacoes$idade)
```

```
[1] 21.4
```

```r
# Informa o valor mediano do conjunto
median(informacoes$idade)
```

```
[1] 19
```

O comando `quantile()` oferece a possibilidade de obter os quartis dos dados de acordo com as probabilidades estabelecidas pelo pesquisador. No exemplo, explora-se a vari�vel idade:


```r
quantile(informacoes$idade,  probs = c(0.5, 1, 2, 5, 10, 50)/100)
```

```
 0.5%    1%    2%    5%   10%   50% 
18.02 18.04 18.08 18.20 18.40 19.00 
```

## Convers�o de datas

A configura��o e padroniza��o dos formato de datas no RStudio podem ser efetuadas pelo pesquisador, primeiramente ao carregar a base de dados no programa e em um segundo momento durante a manipula��o das informa��es. Assim, seguem alguns dos procedimentos para a correta altera��o dos padr�es de datas:


```r
abertura <- c("03/02/69", "17/08/67")
fechamento <- c("2000-20-01", "1999-14-08")
abertura <- as.Date(abertura, format = "%d/%m/%y")
fechamento <- as.Date(fechamento, format = "%Y-%d-%m")

# Diferen�a de dias dos intervalos informados
abertura-fechamento
```

```
Time differences in days
[1] -11308  24840
```

## Exerc�cios

**1.**	Baixe o arquivo "arvores" que se encontra no endere�o <https://smolski.github.io/softwarelivrer/atividades>. Este � um banco de dados com informa��es cedido pela professora Tatiane Chassot. Abra o arquivo no Rstudio tomando os cuidados necess�rios (importar no formato correto, prestar aten��o nas v�rgulas e nomes...). Por meio dos comandos do R, responda as seguintes perguntas, informando o comando utilizado.

**1.1.**	Qual � a esp�cie de �rvore que possui o maior e menor di�metro?  E quais s�o estes valores de di�metro?

<!--
Neste caso, ir�o utilizar o comando da seguinte forma >Nome_do_banco_de_dados$Nome_da_vari�vel_buscada[which.max(di�metro_cm)]
-->

**1.2.**	Qual � a altura m�dia, m�nima e m�dia das �rvores? 

**1.3.**	Encontre o di�metro m�dio para cada esp�cie de �rvores.

**1.4.**	Com os comandos do R, verifique a quantidade de dados referente as vari�veis, bem como o nome referente a cada vari�vel.

**1.5.**	Renomeie a primeira coluna para "esp�cie".

**1.6.**	Classifique as �rvores quanto ao seu porte, em rela��o � altura, em que:

Pequeno porte = �rvores com altura inferior a 10 metros.

Grande porte = �rvores com altura superior a 10 metros. 


**2.**	Baixe o arquivo "bancodedados1" que se encontra no endere�o <https://smolski.github.io/softwarelivrer/atividades>. Este � um banco de dados com informa��es fict�cias que usaremos a fim de aprendizado. Abra o arquivo no Rstudio tomando os cuidados necess�rios. Por meio dos comandos do R, responda as seguintes perguntas, informando o comando utilizado.

**2.1.** Qual � o vendedor com mais sucesso de vendas?  E o vendedor com menor n�mero de vendas?

**2.2.**	Qual foi o n�mero total de vendas?

**2.3.**	Supondo que um vendedor tenha ficado de fora dos dados, insira suas informa��es no banco de dados que j� possu�mos.

- Vendedor = Silvia; Idade = 48; Setor = 2; N de vendas = 45.

**2.4.**	Crie uma nova coluna classificando os vendedores como:

- vendas $<$ 25 = "Regular"

- 25 $>$ vendas = "�timo"

**2.5** Renomeie a coluna "vendas mensais" para "vendas di�rias".


# Estat�stica Descritiva{#desc}

*Denize Ivete Reis*

\begin{flushright}
\emph{}
\end{flushright}

A Estat�stica � uma ci�ncia cujo campo de aplica��o estende-se a diferentes �reas do conhecimento humano. Tem por objetivo fornecer m�todos e t�cnicas que permitem lidar, racionalmente, com situa��es sujeitas a incertezas. Apresenta um conjunto de t�cnicas e m�todos de pesquisa que envolvem o planejamento de estudos (experimentais e observacionais), a coleta e organiza��o de dados, a infer�ncia, a an�lise e a dissemina��o de informa��o.

Alguns termos extensamente utilizados em estat�stica, s�o definidos a seguir [@triola1999]:

**Popula��o**: � uma cole��o completa de todos os elementos (valores, pessoas, medidas etc.) a serem estudados.

**Censo**:  � uma cole��o de dados relativos a todos os elementos de uma popula��o.

**Amostra**:  � uma sub-cole��o de elementos extra�dos de uma popula��o.
	Par�metro  � a medida num�rica que descreve uma caracter�stica de uma popula��o.
	
**Estat�stica**: � uma medida num�rica que descreve uma caracter�stica de uma amostra.


## Natureza da medida das vari�veis


Vari�veis reporta-se a caracter�sticas ou atributos que podem tomar diferentes valores ou categorias, o que se op�e ao conceito de constante [@almeida2000]. Assim, vari�vel pode ser definida como sendo a caracter�stica dos elementos da amostra ou da popula��o que nos interessa estudar estatisticamente.

Vari�veis podem ser classificadas da seguinte forma:

**Vari�veis quantitativas**: consistem em n�meros que representam contagens ou medidas. Dividem-se em:


a) Vari�veis discretas: resultam em um conjunto finito de valores poss�veis, ou de um conjunto enumer�vel desses valores. Ex. n�mero de unidades produzidas.

b) Vari�veis cont�nuas: resultam de um n�mero infinito de valores poss�veis que podem ser associados a pontos em uma escala cont�nua de tal maneira que n�o haja lacunas ou interrup��es. Ex. Renda das fam�lias em reais.

**Vari�veis qualitativas**: ou vari�veis categ�ricas, ou atributos que podem ser separados em diferentes categorias que se distinguem por alguma caracter�stica n�o-num�rica. Divididas em:

a) Vari�vel nominal: caracterizada por dados que consistem apenas em nomes, r�tulos ou categorias. Os dados n�o podem ser dispostos segundo um esquema ordenado (como de baixo para cima). Ex. nacionalidade

b) Vari�vel ordinal: envolve vari�veis representadas por nomes que podem ser dispostos em alguma ordem, mas as diferen�as entre os valores dos dados n�o podem ser determinadas, ou n�o tem sentido. Esse n�vel d� informa��es sobre compara��es relativas, mas os graus de diferen�a n�o servem para c�lculos [@triola1999]. Ex. Grau de escolaridade.

**Dado**: � o valor assumido por uma vari�vel aleat�ria em um experimento.


A Estat�stica subdivide-se em descritiva e inferencial. A estat�stica descritiva se preocupa em descrever os dados. A estat�stica inferencial, fundamentada na teoria das probabilidades, se preocupa com a an�lise destes dados e sua interpreta��o.

Informa��es estat�sticas em jornais, relat�rios e outras publica��es que consistem de dados reunidos e apresentados de forma clara e resumida, na forma de tabelas, gr�ficos ou num�ricos, s�o conhecidos como estat�sticas descritivas (ANDERSON, 2002).


**Exemplo 1**

Estaremos utilizando como exemplo os dados de uma pesquisa (dados simulados), cujo banco de dados est� intitulado "Dados\_pesquisa.ods". Os dados s�o referentes aos resultados obtidos por ocasi�o de uma pesquisa realizada entre os consumidores a fim de analisar caracter�sticas associadas ao mercado consumidor de sucos, sendo que a amostra � composta de 348 entrevistados aleatoriamente selecionados.


- O objetivo prim�rio do estudo foi determinar vari�veis que seriam �teis para caracterizar os consumidores que j� conhecem o suco e a possibilidade potencial de futuros consumidores. H� tamb�m interesse nas rela��es entre vari�veis das caracter�sticas pessoais desses consumidores ou futuros consumidores.

- A pesquisa foi realizada, depois que os participantes realizaram uma visita t�cnica �s instala��es da empresa e puderam conhecer seus produtos e processos.

Para cada entrevistado foram registrados dados para as seguintes vari�veis:
 

**Sexo** � G�nero sexual;

**Divulgacao** � Forma de acesso ao suco ou publicidade do mesmo;

**Renda\_h** � Renda por hora do entrevistado;

**Praticidade** � Aspectos quanto a oferta do suco, como por ex. embalagem;

**Sabor** � Aspectos relacionados ao sabor;

**Pessoas\_familia** � N�mero de pessoas que comp�e o grupo familiar;

**Pre�o** � como cada entrevistado classificava o pre�o do produto;

**consumo\_anterior** � Se j� consumia o suco antes da visita t�cnica;

**consumo\_pos** � Se consumia o suco ap�s a visita t�cnica;

**Idade** � Idade dos consumidores;

**Altura\_(m)** � Altura dos consumidores;

**Peso\_(Kg)** � Peso dos consumidores.

Pede-se:

1.	Salvar inicialmente os dados em formato CSV, xlsx ou outro.

2.	Ler os dados no "Environment" pelo "Import Dataset...From CSV" ou outro. No exemplo abaixo foram importados os dados diretamente do arquivo hospedado na internet.

3.	Carregar o banco de dados, com a finalidade de usar os objetos (vari�veis) diretamente nas fun��es a serem utilizadas.

`attach(nome_da_planilha)`
  

```r
library(readxl)
url <- "https://github.com/Smolski/livror/raw/master/pesquisa_dados.xlsx"
destfile <- "pesquisa_dados.xlsx"
curl::curl_download(url, destfile)
pesquisa_dados <- read_excel(destfile)
attach(pesquisa_dados)
ls.str(pesquisa_dados)
```

```
Altura_(m) :  num [1:348] 1.82 1.9 1.69 1.89 1.9 1.76 1.83 1.81 1.67 1.55 ...
Caso :  num [1:348] 1 2 3 4 5 6 7 8 9 10 ...
consumo_anterior :  chr [1:348] "N" "N" "S" "N" "S" "S" "S" "N" "N" "N" "N" "N" "S" "S" "S" ...
consumo_pos :  chr [1:348] "N" "S" "N" "S" "N" "S" "N" "S" "N" "S" "S" "S" "S" "S" "S" ...
Divulgacao :  chr [1:348] "Degustacao" "Radio" "TV" "TV" "Degustacao" "TV" "TV" "Radio" ...
Idade :  num [1:348] 22 21 20 18 16 28 19 19 22 19 ...
Peso_(Kg) :  num [1:348] 78.5 80 54 78 36 82 75 69 58 49 ...
Pessoas_familia :  num [1:348] 4 3 3 7 4 4 3 4 1 4 ...
Praticidade :  chr [1:348] "Pessima" "Otima" "Boa" "Pessima" "Ruim" "Boa" "Regular" ...
Pre�o :  chr [1:348] "Acima_concorrencia" "Abaixo_concorrencia" ...
Renda_h :  chr [1:348] "1.41" "17.34" "6.86" "2.65" "2.01" "11.32" "6.86" "3.25" ...
Sabor :  chr [1:348] "Otimo" "Pessimo" "Bom" "Otimo" "Otimo" "Regular" "Ruim" "Bom" ...
Sexo :  chr [1:348] "Feminino" "Feminino" "Feminino" "Feminino" "Masculino" ...
```
  
## Tabelas

Segundo @barbetta1988, dados representados em tabelas e gr�ficos adequados, permitem observar determinados aspectos relevantes, bem como delinear hip�teses a respeito da estrutura dos dados em estudo, o que conhecemos como an�lise explorat�ria de dados. Isto pode ser feito inicialmente com a representa��o em forma de tabelas.


O comando `table()` � utilizado para elaborarmos tabelas de frequ�ncias absolutas. Dependendo da vari�vel a ser representada, podemos usar esse comando de diferentes formas:

### Tabela simples para apresenta��o das frequ�ncias absolutas

Uma tabela simples considera quantas vezes ocorre cada categoria (ou n�vel).

`table(nome_vari�vel)`


Ex. Vari�vel **Praticidade**


```r
table(Praticidade)
```

```
Praticidade
    Boa   Otima Pessima Regular    Ruim 
     82      70      21      80      95 
```

### Tabela cruzada

A tabela cruzada, tamb�m conhecida como tabela de dupla entrada, para apresenta��o das frequ�ncias absolutas.


`table(nome_vari�vel1,nome_vari�vel2)`


Ex. Construir uma tabela cruzada apresentando as frequ�ncias absolutas das vari�veis **Sexo** e **Divulgacao**.


```r
table(pesquisa_dados$Sexo,pesquisa_dados$Divulgacao)
```

```
           
            Degustacao Outro Radio  TV
  Feminino          78     6    61 147
  Masculino         19     1    15  21
```


### Tabela cruzada para apresenta��o das frequ�ncias relativas

Com a introdu��o do comando `prop.table` � poss�vel gerar, facilmente, tabelas de frequ�ncias relativas para as vari�veis de interesse. As medidas relativas s�o importantes para comparar distribui��es de frequ�ncias [@barbetta1988].

`prop.table(table(nome_vari�vel1,nome_vari�vel2))`


Ex. Construir uma tabela cruzada apresentando as frequ�ncias relativas das vari�veis **Sexo** e **Divulgacao**.


```r
prop.table(table(Divulgacao,Sexo))
```

```
            Sexo
Divulgacao   Feminino Masculino
  Degustacao 0.224138  0.054598
  Outro      0.017241  0.002874
  Radio      0.175287  0.043103
  TV         0.422414  0.060345
```


A fun��o `tapply` serve para calcular um valor usando uma vari�vel categ�rica como condi��o, ou seja, aplica uma fun��o qualquer (como m�dia, por exemplo) a uma vari�vel quantitativa para cada classe de uma vari�vel categ�rica. Assim, permite obter em um s� comando, a medida para cada categoria. 

`tapply(var_quantitativa,var_categ�rica, fun��o_desejada)`

`tapply(variavel_quantitativa,variavel_qualitativa, mean)`

Se um registro possui `NA`, isto �, dados perdidos: com o par�metro na.rm=T, indicamos para o comando ignorar os NAs nos dados e calcular a m�dia. 


`tapply(variavel_quanti, variavel_quali, mean, na.rm=T)`

## Gr�ficos

### Gr�fico de colunas

As frequ�ncias podem ser visualizadas graficamente, usando gr�ficos de barras elementares, que se aplicam � descri��o de qualquer vari�vel qualitativa ou quantitativa discreta, vetor de dados ou tabelas.

No entanto, no caso de dados em banco de dados, quando n�o utilizamos outros mecanismos de atribui��o, precisamos usar o comando table.

`barplot(table(nome_vari�vel))`

Ex. Construir um gr�fico de colunas para a vari�vel **Sexo**.


```r
barplot(table(Sexo))
```

<div class="figure" style="text-align: center">
<img src="index_files/figure-html/unnamed-chunk-67-1.png" alt="Gr�fico de colunas com a vari�vel Sexo" width="80%" />
<p class="caption">(\#fig:unnamed-chunk-67)Gr�fico de colunas com a vari�vel Sexo</p>
</div>

**Obs**.: � poss�vel personalizar o gr�fico, incluindo o t�tulo do eixo x (xlab), o t�tulo do eixoy (ylab), o t�tulo do gr�fico (main), a cor da coluna (col) e cor da borda da coluna (border), lembrando que as cores, assim como os comandos devem ser expressas em ingl�s.


`barplot(table(nome_vari�vel), col=c("blue","red"), main="T�tulo", xlab="Vari�vel do eixo x", ylab = "Informa��o que consta no eixo y",border="red")`


**Ex.1)** Construir um gr�fico de colunas para a vari�vel **Pessoas\_familia**.



```r
barplot(table(`Pessoas_familia`), col=c("blue"), 
        main = "Frequ�ncia de pessoas por fam�lia", 
        xlab = "Frequ�ncia", 
        ylab = "Pessoas", 
        border = "red")
```

<div class="figure" style="text-align: center">
<img src="index_files/figure-html/unnamed-chunk-68-1.png" alt="Gr�fico de colunas com a vari�vel `Pessoas familia`" width="80%" />
<p class="caption">(\#fig:unnamed-chunk-68)Gr�fico de colunas com a vari�vel `Pessoas familia`</p>
</div>

**Ex.2)** Construir uma tabela de dupla entrada para as vari�veis **Sexo** e **Divulga��o**.


```r
barplot(table(Sexo,Divulgacao), 
        col=c("blue"), 
        main = "Frequ�ncia de pessoas por Sexo e Divulgacao")
```

<div class="figure" style="text-align: center">
<img src="index_files/figure-html/unnamed-chunk-69-1.png" alt="Gr�fico de colunas com as vari�veis Sexo e Divulgacao" width="80%" />
<p class="caption">(\#fig:unnamed-chunk-69)Gr�fico de colunas com as vari�veis Sexo e Divulgacao</p>
</div>


**Ex.3)** Na sequ�ncia utiliza o sinal de atribui��o <- para atribuir o nome Resultado para esta tabela (tabela de dupla entrada obtida em Ex.2).


```r
Resultado<-table(Sexo,Divulgacao)
```

**Ex.4)** Execute o seguinte comando:


```r
barplot(Resultado,col=c("blue","red"),main="T�tulo",
        xlab="Vari�vel do eixo x",
        ylab="Informa��o que consta no eixo y", 
        border='red', 
        beside=T,legend=rownames(Resultado),
        args.legend = list(x = "topleft"))
```

<div class="figure" style="text-align: center">
<img src="index_files/figure-html/unnamed-chunk-71-1.png" alt="Gr�fico de colunas com as vari�veis Sexo e Divulgacao (2)" width="80%" />
<p class="caption">(\#fig:unnamed-chunk-71)Gr�fico de colunas com as vari�veis Sexo e Divulgacao (2)</p>
</div>


Observe que o uso do argumento `beside=T` evita que as barras fiquem empilhadas e o arguemnto `legend`' insere a legenda conforme as cores das colunas.


**Ex.5)** Repita o exerc�cio a partir do Ex.3, invertendo a ordem entre as vari�veis qualitativas.

### Setograma ou gr�fico de pizza

Os gr�ficos em setores s�o utilizados para ilustrar dados qualitativos de modo mais compreens�vel. Quando a vari�vel � ordinal, gr�ficos de colunas s�o mais indicados pelo fato de permitirem manter a ordem das categorias. Isto tamb�m vale para os casos em que se tem muitas categorias ou quanto se pretende dar mais destaque �s categorias mais frequentes [@barbetta1988].

`pie(table(nome_vari�vel),main="nome")`

Ex. Construa um gr�fico na forma de Setograma para a vari�vel **Sabor**.


```r
# Criar objeto com a tabela de Sabor
Sabor1=table(Sabor)

# Calcular o percentual
percent=signif(Sabor1/sum(Sabor1)*100,3)

#Criando os nomes da legenda
nomesleg=c("Bom","�timo","P�ssimo","Regular","Ruim")

#Plota-se o gr�fico de pizza
pie(Sabor1, 
    labels = paste(percent, "%", sep=""), 
    col = terrain.colors(5), # Determina cores 
    radius = 1) 
legend(x="topright", # Determina posi��o da legenda
       legend=nomesleg, # Insere nomes da legenda
       cex = 0.65, # Tamanho do texto
       fill = terrain.colors(5)) # Determina cores 

## Alguns exemplos de paletas de cores:
# - rainbow(n)
# - heat.colors(n)
# - terrain.colors(n) 
# - topo.colors(n)
# - cm.colors(n)
```

<div class="figure" style="text-align: center">
<img src="index_files/figure-html/unnamed-chunk-72-1.png" alt="Gr�fico de pizza com a vari�vel Sabor" width="80%" />
<p class="caption">(\#fig:unnamed-chunk-72)Gr�fico de pizza com a vari�vel Sabor</p>
</div>

### Histograma

No histograma, utilizado em geral quando temos vari�veis quantitativas cont�nuas, a altura dos ret�ngulos representa a frequ�ncia de ocorr�ncia de valores no intervalo (deve iniciar sempre em zero), devem ter sempre a mesma largura podendo ser justapostos. O eixo horizontal (dos valores da vari�vel) pode iniciar pr�ximo ao menor valor da vari�vel [@barbetta1988]. Para confec��o do histograma devemos usar:

`hist(nome_vari�vel)`

Ex. Construa um histograma com a vari�vel **Renda\_h**.


```r
hist(as.numeric(`Renda_h`))
```

<div class="figure" style="text-align: center">
<img src="index_files/figure-html/unnamed-chunk-73-1.png" alt="Histograma com a vari�vel `Renda h`" width="80%" />
<p class="caption">(\#fig:unnamed-chunk-73)Histograma com a vari�vel `Renda h`</p>
</div>

**Obs**. I: Neste caso tamb�m � poss�vel personalizar o gr�fico, incluindo o t�tulo do eixo x (xlab), o t�tulo do eixoy (ylab), o t�tulo do gr�fico (main), a cor da coluna (col) e cor da borda da coluna (border), lembrando que as cores, assim como os comandos devem ser expressas em ingl�s.

**Obs**. II: Para definir o n�mero de intervalos no Histograma, usamos:


`hist(nome_vari�vel, breaks = 5)`


```r
hist(as.numeric(`Renda_h`), 
     breaks=5, 
     labels=TRUE, 
     ylim=c(0,200), 
     xlab = 'Renda',
     ylab = 'Frequ�ncia',
     main = 'Histograma da Renda',
     col = '#BBDEFB')
```

<div class="figure" style="text-align: center">
<img src="index_files/figure-html/unnamed-chunk-74-1.png" alt="Histograma com a vari�vel Renda h com breaks=5" width="80%" />
<p class="caption">(\#fig:unnamed-chunk-74)Histograma com a vari�vel Renda h com breaks=5</p>
</div>
O comando `ylim` determina os limites do eixo y a serem mostrados; `xlab` e `ylab` determinam o nome das vari�veis dos eixos x e y; `main` determina o nome do t�tulo e `col` determina a cor do gr�fico. Use o argumento `main=NULL` para remover o t�tulo.

Inserindo as op��es `$counts` e `$breaks` retomamos os valores da contagem dos dados e dos intervalos do histograma:


```r
hist(as.numeric(`Renda_h`), breaks=5)$counts
```

```
[1] 106 167  62  11   2
```

```r
hist(as.numeric(`Renda_h`), breaks=5)$breaks
```

<img src="index_files/figure-html/unnamed-chunk-75-1.png" width="80%" style="display: block; margin: auto;" />

```
[1]  0  5 10 15 20 25
```


### Boxplot ou diagrama em caixas

Os diagramas em caixa s�o convenientes para revelar tend�ncias centrais, dispers�o, distribui��o dos dados e a presen�a de outliers (valores extremos). Como as medianas revelam uma tend�ncia central, ao passo que os quartis indicam a dispers�o dos dados, os diagramas em caixa t�m a vantagem de n�o serem t�o sens�veis a valores extremos como outras medidas baseadas na m�dia e no desvio-padr�o. Por outro lado, os diagramas em caixa (boxplots) n�o d�o informa��o t�o detalhada quanto os histogramas ou os gr�ficos ramo-e-folhas, podendo n�o ser, assim, a melhor escolha quando lidamos com um �nico conjunto de dados. Os diagramas em caixa s�o, entretanto, mais convenientes na compara��o de dois ou mais conjuntos de dados [@triola1999]. 

No diagrama de caixas, torna-se f�cil identificar **outliers** (ou valores extremos), que s�o valores extremamente  raros, no sentido de que est�o muito afastados da maioria dos dados. Ao explorarmos um conjunto de dados, n�o podem deixar de considerar os outliers, porque eles podem revelar informa��es importantes [@triola1999].

Para obter o boxplot para um conjunto de dados:

`boxplot(vari�velA, vari�velB, names=c("A","B"))`


**Ex.1)** Construir um boxplot da vari�vel **Idade**.


```r
boxplot(Idade,horizontal = T)
```

<div class="figure" style="text-align: center">
<img src="index_files/figure-html/unnamed-chunk-76-1.png" alt="Boxplot com a vari�vel Idade" width="80%" />
<p class="caption">(\#fig:unnamed-chunk-76)Boxplot com a vari�vel Idade</p>
</div>


**Ex.2)** Construir um boxplot das vari�veis **Peso\_(Kg)** e **Altura\_(m)**.    



### Gr�fico ramo-e-folhas

Em um gr�fico ramo-e-folhas, classificamos os dados segundo um padr�o que revela a distribui��o subjacente. O padr�o consiste em separar um n�mero em duas partes em geral: o ramo consiste nos algarismos mais � esquerda e as folhas consistem nos algarismos mais � direita.

No gr�fico Ramo-e-folhas, podemos ver a distribui��o desses dados, que � uma vantagem do gr�fico ramo-e-folhas e ainda conservar toda a informa��o da lista original; se necess�rio, podemos recompor a rela��o original de valores. Note que as linhas de algarismos em um gr�fico ramo-e-folhas s�o an�logas, em natureza, �s barras de um histograma [@triola1999].


`stem(nome_vari�vel)` - comando que permite obter um gr�fico Ramo e Folhas. 

Ou 

`stem(nome_vari�vel,scale=1)`


O "scale=1", que � o padr�o, separa os ramos das folhas a partir das casas decimais.

Caso padr�o:

- A ideia do ramo e folhas � separar um n�mero (como 16,0) em duas partes. Assim, a primeira parte inteira (16) chamada de ramo e a segunda, a parte decimal (0) chamada de folha. O padr�o do R � separar os n�meros em duas partes (inteira e decimal) e agrupar os n�meros em classes de tamanho 2. Por exemplo, o ramo 16 leva em conta os n�meros 16 e 17. 


**Obs.**: Esse padr�o vai se alterando, � medida que o conjunto de dados apresente diferentes casas decimais.

Assim, outras op��es podem ser avaliadas:

a) `stem(nome_vari�vel,scale=0.5)`

b) `stem(nome_vari�vel,scale=2)`

**Obs.**: Quando uma folha relacionada com certo ramo tem uma quantidade t�o grande de valores que ele sintetiza essa quantidade usando a denomina��o +n, e invade a linha seguinte. Isso pode ser melhorado usando **width**.

c) `stem(nome_vari�vel,scale=0.5,width=120)`

Ex. Construa um gr�fico Ramo e Follhas com a vari�vel **Idade**.


```r
stem(Idade,scale=2)
```

```

  The decimal point is at the |

  16 | 000
  17 | 000000000
  18 | 0000000000000000000000000000000000000000
  19 | 000000000000000000000000000000000000000000000000
  20 | 0000000000000000000000000000000000000000000000000000000000000000
  21 | 000000000000000000000000000000000000000000000000000000000000
  22 | 0000000000000000000000000000000000000000000
  23 | 000000000000
  24 | 000000000
  25 | 0000
  26 | 00000000000
  27 | 00000000000
  28 | 0000000000000
  29 | 00
  30 | 00000
  31 | 
  32 | 00
  33 | 
  34 | 00
  35 | 00
  36 | 
  37 | 
  38 | 000
  39 | 
  40 | 
  41 | 
  42 | 
  43 | 
  44 | 
  45 | 
  46 | 
  47 | 
  48 | 00000
```

### Gr�ficos de dispers�o

�s vezes temos dados emparelhados de forma que associa cada valor de um conjunto a um determinado valor de um segundo conjunto. Um diagrama de dispers�o � um gr�fico dos dados emparelhados (x, y), com um eixo x horizontal e um eixo y vertical. O diagrama de dispers�o, apresenta no eixo horizontal os valores da primeira vari�vel e um eixo vertical para os valores da segunda vari�vel. O padr�o dos pontos assim marcados costuma ajudar a determinar se existe algum relacionamento entre as duas vari�veis A e B.

`plot(vari�vel_independente,Vari�vel_dependente)`

Ou

`plot(vari�vel_dependente~vari�vel_independente)`

### Gr�fico de linhas

Apresenta a evolu��o de um dado, geralmente ao longo do tempo. Eixos na vertical e na horizontal indicam as informa��es a que se refere e a linha tra�ada entre eles, ascendente, descendente constante ou com v�rios altos e baixos mostra o percurso de um fen�meno espec�fico.

Ex. Considere os dados que descrevem os valores do n�mero de empresas fiscalizadas na fiscaliza��o do trabalho na �rea rural Brasil 1998-2010.

<!--

Table: (\#tab:unnamed-chunk-78)Evolu��o dos resultados da fiscaliza��o do trabalho na �rea rural Brasil 1998-2010

  Ano  Empresas.Fiscalizadas 
-----  ----------------------
 1998  7.042                 
 1999  6.561                 
 2000  8.585                 
 2001  9.641                 
 2002  8.873                 
 2003  9.367                 
 2004  13.856                
 2005  12.192                
 2006  13.326                
 2007  13.390                
 2008  10.839                
 2009  13.379                
 2010  11.978                
-->

Table: (\#tab:evolres)Evolu��o dos resultados da fiscaliza��o do trabalho na �rea rural Brasil 1998-2010

|**Ano**|**Empresas Fiscalizadas**|
|:----:|:---------------------:|
| 1998|7.042                  |
| 1999|6.561                  |
| 2000|8.585                  | 
| 2001|9.641                  |
| 2002|8.873                  |
| 2003|9.367                  |
| 2004|13.856                 |
| 2005|12.192                 |
| 2006|13.326                 |
| 2007|13.390                 |
| 2008|10.839                 |
| 2009|13.379                 |
| 2010|11.978                 |

Fonte: MTE. SFIT. Elabora��o: DIEESE.

Para construir um gr�fico de linhas, utilizamos o seguinte comando:

`plot(x,y,type= "Tipo de s�mbolo")`

Neste gr�fico, podemos utilizar comandos j� utilizados anteriormente, para inserir t�tulo, nomes dos eixos, etc. Para escolher o formato das linhas, com o uso do argumento `type`, seguem algumas op��es:

- `"p"` para pontos,
- `"l"` para linhas,
- `"b"` para pontos e linhas,
- `"c"` para linhas descont�nuas nos pontos,
- `"o"` para pontos sobre as linhas,
- `"n"` para nenhum gr�fico, apenas a janela.

Para o caso de representa��o no mesmo gr�fico, de duas ou mais vari�veis, o processo dever� ser realizado por etapas:

`plot(x,y1,type="b",main="T�tulo", xlab="Nome_eixo_x",ylab="Nome_eixo_y", col="cor das linhas",ylim=c(yi,ys))`


```r
empfisc=data.frame(ano=c(1998,1999,2000,2001,2002,2003,2004,2005,2006,2007,
    2008,2009,2010), qtd=c(7042,6561,8585,9641,8873,9367,
13856,12192,13326,13390,10839,13379,11978))

plot(empfisc$ano,empfisc$qtd,type="b",main="T�tulo",
     xlab="Nome_eixo_x",ylab="Nome_eixo_y", 
     col="blue",xlim=c(1998,2010))
```

<div class="figure" style="text-align: center">
<img src="index_files/figure-html/unnamed-chunk-79-1.png" alt="Gr�fico de linha sobre a fiscaliza��o do trabalho na �rea rural Brasil 1998-2010" width="80%" />
<p class="caption">(\#fig:unnamed-chunk-79)Gr�fico de linha sobre a fiscaliza��o do trabalho na �rea rural Brasil 1998-2010</p>
</div>

onde, no argumento `ylim`, devemos indicar o intervalo de varia��o dos valores de y, ou seja todo o intervalo que ser� necess�rio para representar todas as vari�veis.

Na sequ�ncia adicionamos as instru��es para as demais vari�veis:

`lines(x, y2,col="cor_desejada", type="b")`

Com o argumento `"legend"` instru�mos a formata��o da legenda:

`legend(xp,yp,c("representa��o_vari�vel_1 na legenda", "representa��o_vari�vel_2 na legenda"),
`col =c("Cor1","cor2"),pch=Valor entre 0 e 25)`

Obs.: `pch`= n�mero (entre 0 e 25). No Help do R (buscando com pch), voc� encontra a lista completa de s�mbolos que podem ser utilizados na representa��o da legenda.
Neste caso, pode ser importante tamb�m alterar o tamanho da fonte da legenda, com o uso do argumento `"cex"`.

Exemplo: Segue exemplo de um gr�fico de linhas para as temperaturas registradas durante o dia 11/04/2018, pela Esta��o Meteorol�gica de S�o Luiz Gonzaga, RS, conforme dados obtidos no site do Inmet.































































































































































































































