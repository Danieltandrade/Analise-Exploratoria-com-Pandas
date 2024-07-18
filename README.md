# Analise-Exploratoria-com-Pandas

- Curso: Python Development
- Módulo: Análise Exploratória com Pandas
- Instrutor: Fernanda Santos
- Instituição: [DIO.me](https://www.dio.me/)
- Editor de Código: Google Colab

Neste projeto utilizei o Google Colab para realizar uma análise exploratória utilizando a biblioteca __Pandas__.
O arquivo "Analise_Exploratoria_com_Pandas.ipynb" está presente nos arquivos do projeto, mostrando a lógica empregada para resolver este desafio.

## Criando Repositório

Primeiramente criei o repositório no __GitHub__ com nome __"Analise-Exploratoria-com-Pandas"__ e clonei o repositório para meu PC utilizando o __GitHub Desktop__.

## Desafio

O desafio consiste em realizar uma análise exploratória utilizando a biblioteca __Pandas__.
Também utilizei em meu projeto as bibliotecas de visualização de dados: __Matplotlib__ e __Seaborn__.

O arquivo utilizado para a análise exploratória foi o arquivo __AdventureWorks.xlsx__, que foi disponibilizado pelo instrutor.

- Primeiramente foi criado um DataFrame para o início da manipulação dos dados, com a linha de código apresentada abaixo:

```
df = pd.read_excel('AdventureWorks.xlsx')
```

- Foram executadas várias linhas de comando, explorando os recursos da biblioteca __Pandas__ e demonstrando o seu poder para a realização de análises de dados. Alguns comando estão listados abaixo:

    - df.head()
    - df.shape
    - df.dtypes
    - df['Valor Venda'].sum()
    - df.groupby('Marca')['Tempo_envio'].mean()
    - df.isnull().sum()

- Também foram criadas novas colunas no DataFrame, com o objetivo de obter informações que não estavam disponível no arquivo original. Os códigos para criação destas colunas estão listados abaixo:

    - df['Custo'] = df['Custo Unitário'].mul(df['Quantidade']) # Criando coluna de custo.
    - df['Lucro'] = df['Valor Venda'] - df['Custo'] # Criando coluna de Lucro.
    - df['Tempo_envio'] = df['Data Envio'] - df['Data Venda'] # Criando coluna com total de dias para enviar o produto.

- Após a exploração dos recursos da biblioteca __Pandas__ criei alguns gráficos, que nos apresentam informações sobre a análise exploratória de dados. Para isso foram utilizados comando da biblioteca __Matplotlib__, com alguns destes comandos listados abaixo:

    - df.groupby('Produto')['Quantidade'].sum().sort_values(ascending=True).plot.barh(title='Total de Produtos Vendidos')
    plt.xlabel('Total')
    plt.ylabel('Produto');
    - df.groupby(df['Data Venda'].dt.year)['Lucro'].sum().plot.bar(title='Lucro por Ano')
    plt.xlabel('Ano')
    plt.ylabel('Receita');
    - df_2009.groupby(df_2009['Data Venda'].dt.month)['Lucro'].sum().plot(title='Lucro x Mês')
    plt.xlabel('Mês')
    plt.ylabel('Lucro');

## Conclusão

Este foi mais um projeto de __Liguagem Python__ dentro do curso __Python Development__ e foi a primeira vez que tive contato com as bibliotecas __Pandas__ e __Matplotlib__. Achei muito interessante conhecer uma pouco mais sobre essas bibliotecas e para mim que pretendo migrar para área de dados, este primeiro contato me deixou ainda mais anciosos por novos desafios nesta área.

Grande abraço a todos!!!

## Linguagens de Marcação e Programação

- ![Markdown](https://img.shields.io/badge/Markdown-000?style=for-the-badge&logo=markdown)

- ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

## Ferramentas e Serviços

- ![Git](https://img.shields.io/badge/GIT-E44C30?style=for-the-badge&logo=git&logoColor=white)

- ![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)

- ![Vscode](https://img.shields.io/badge/Vscode-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white)

- ![Colab](https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&color=525252)