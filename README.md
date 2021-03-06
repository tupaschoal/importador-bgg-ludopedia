## Importador BGG - Ludopedia

Script criado para facilitar a importação de coleção (jogos que possui e lista de desejos) e partidas do site [BoardGameGeek][1] para [Ludopedia][2].

### Como usar

#### Usuários básicos

1. Baixar e descompactar a versão correspondente ao seu sistema operacional dos [releases][3]
2. Executar o arquivo chamado ```importador``` 
3. Seguir as instruções na tela

#### Usuários avançados

1. ```git clone https://github.com/dambros/importador-bgg-ludopedia.git```
2. ```cd importador-bgg-ludopedia```
3. ```pip install pipenv```
4. ```pipenv install```
5. ```pipenv shell```
6. ```python3 importador.py```
7. Seguir as instruções na tela

Para fazer release:
1. ```pipenv shell```
2. ```pyinstaller importador.spec --noconfirm --clean```
3. Veja o executável na pasta `dist`

### Limitações

Devido a forma como a Ludopedia está construída atualmente, não há disponível nenhuma API para comunicação com seu servidor. Sendo assim, não há tanto controle em como podemos fazer uma busca e inserção na base.

A Ludopedia utiliza o BGG como insumo para sua base de dados, mas não possui nenhum local onde nos permita fazer uma busca utilizando o *id* do BGG. Isso quer dizer que as buscas são realizadas utilizando o *nome do jogo* e comparando se o *ano de lançamento* bate, por isso alguns jogos não serão adicionados ou pode ocorrer de serem adicionados ítens errados na coleção. Uma janela será exibida com as opções caso não haja correspondência exata.

### Marcando amigos na importação de partidas

Não tendo uma forma automática de identificar outros usuários do BGG na Ludopedia, para marcar amigos nas partidas, uma possibilidade é criar um arquivo `usuarios.txt` neste mesmo diretório, tendo como conteúdo um usuário por linha, no formato `nome_usuario_bgg=id_usuario_ludopedia` ou `nome_usuario_bgg=nome_usuario_ludopedia`. Exemplo:

```
fulano=ciclano
beltrano=12345
```

### Problemas, dúvidas ou sugestões?

Caso tenha qualquer tipo de dúvida, problema ou sugestão, fique a vontade em abrir uma [issue][1] ou deixar uma mensagem no [tópico oficial][2] na Ludopedia que responderei o mais rápido possível.

[1]: https://boardgamegeek.com/
[2]: https://www.ludopedia.com.br/
[3]: https://github.com/dambros/importador-bgg-ludopedia/releases
[4]: https://github.com/dambros/importador-bgg-ludopedia/issues
[5]: https://ludopedia.com.br/topico/24305/importador-de-colecao-bgg-ludopedia
