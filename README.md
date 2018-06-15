## Importador BGG - Ludopedia

Script criado para facilitar a importação de uma coleção (jogos que possúi e lista de desejos) do site BoardGameGeek
para Ludopedia.

### Como usar

#### Usuários básicos

1. Baixar e descompactar a versão correspondente ao seu sistema operacional dos [releases](https://github.com/dambros/importador-bgg-ludopedia/releases)
2. Executar o arquivo chamado ```importador``` 
3. Seguir as instruções na tela

#### Usuários avançados/Linux

1. ```git clone https://github.com/dambros/importador-bgg-ludopedia.git```
2. ```cd importador-bgg-ludopedia```
3. ```pipenv install```
4. ```python3 importador.py```
5. Seguir as instruções na tela

### Limitações

Devido a forma como a Ludopedia está construída atualmente, não há disponível nenhuma API para comunicação com seu servidor. Sendo assim, não há tanto controle em como podemos fazer uma busca e inserção na base.

A Ludopedia utiliza o BGG como insumo para sua base de dados, mas não possui nenhum local onde nos permita fazer uma busca utilizando o *id* do BGG. Isso quer dizer que as buscas são realizadas utilizando o *nome do jogo* e comparando se o *ano de lançamento* bate, por isso alguns jogos não serão adicionados (por exemplo Catan) ou pode ocorrer de ser adicionados ítens errados na coleção.

### Problemas, dúvidas ou sugestões?

Caso tenha qualquer tipo de dúvida, problema ou sugestão, fique a vontade em abrir uma [issue](https://github.com/dambros/importador-bgg-ludopedia/issues) ou deixar uma mensagem no [tópico oficial](https://ludopedia.com.br/topico/24305/importador-de-colecao-bgg-ludopedia) na Ludopedia que responderei o mais rápido possível.