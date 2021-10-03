# Projeto MySQL One for All

Projeto feito como critério avaliativo na escola de programação **Trybe**.

O projeto é a criação de um banco de dados através de uma tabela fornecida. Nessa tabela foi aplicada a normalização para que seja possível a utilização de um banco de dados relacional para armazenar seus dados. Após a normalização, foi criando o banco bem como suas tabelas e a população de seus dados. Foram criadas várias VIEWs de acordo com a necessidade dos requisitos, bem como PROCEDURES, FUNCTIONS e TRIGGERS utilizando o MySQL Workbench.

## Instruções para reproduzir o projeto

### Pré requisitos

1. Possuir `mysql-server` e `MySQL Workbench` instalados

2. Clone o repositório
  * `git clone git@github.com:Kevin-Ol/project-mysql-one-for-all.git`.
  * Entre na pasta do repositório que você acabou de clonar:
    * `cd project-mysql-one-for-all`

3. Instale as dependências
  * `npm install`

---

### Instruções para testar queries

Para executar localmente os testes, é preciso escrever o seguinte no seu terminal:
```sh
MYSQL_USER=<SEU_NOME_DE_PESSOA_USUARIA> MYSQL_PASSWORD=<SUA SENHA> HOSTNAME=<NOME_DO_HOST> npm test
```

Ou seja, suponha que para poder acessar a base de dados feita neste projeto você tenha `root` como seu nome de pessoa usuária, `password` como senha e `localhost` como host. Logo, você executaria:
```sh
MYSQL_USER=root MYSQL_PASSWORD=password HOSTNAME=localhost npm test
```

Usando o exemplo anterior de base, suponha que você não tenha setado uma senha para `root`. Neste caso, você executaria:
```sh
MYSQL_USER=root MYSQL_PASSWORD= HOSTNAME=localhost npm test
  ```

## Requisitos do projeto 

1 - Crie um banco com o nome de `SpotifyClone` através da normalização da tabela abaixo:

![Tabela não normalizada "Spotify Clone"](./images/non-normalized-tables.png)
[Faça o download da tabela aqui](./SpotifyClone-Non-NormalizedTable.xlsx)

2- Crie uma VIEW chamada `estatisticas_musicais` exibindo a quantidade total de canções, artistas e álbuns;

3- Crie uma VIEW chamada `historico_reproducao_usuarios` exibindo os usuários e o nome das respectivas músicas ouvidas de acordo com o seu histórico. Os resultados devem ser ordenados alfabeticamente de acordo com o nome do usuário, seguido pelo nome da canção;

4 - Crie uma VIEW com o nome `top_3_artistas` que deve mostrar somente as três pessoas artistas mais populares no banco SpotifyClone. Os resultados devem ser ordenados pela maior quantidade de seguidores, seguido pela ordenação alfabética do nome dos artistas;

5 - Crie uma VIEW chamada `top_2_hits_do_momento` exibindo as 2 músicas mais ouvidas. Os resultados devem ser ordenados pela maior quantidade de reproduções, seguido pela ordenação alfabética do nome das canções;

6 - Crie uma VIEW chamada `faturamento_atual` exibindo o faturamento mensal da empresa, contendo as colunas faturamento minimo, faturamento maximo, faturamento medio e faturamento total. Os valores devem ser arredondados para 2 casas decimais;

7 - Crie uma VIEW chamada `perfil_artistas` exibindo o nome dos artistas, os álbuns produzidos e o número de seguidores por álbum. Os resultados devem ser ordenados pela maior quantidade de seguidores, seguido pela ordenação alfabética do nome dos artistas e ordenação alfabética do nome dos álbuns;

8 - Crie uma TRIGGER chamada `trigger_usuario_delete` que deve ser disparada sempre que uma pessoa usuária for excluída do banco de dados, refletindo essa exclusão em todas as tabelas que ela estiver;

9 - Crie uma PROCEDURE chamada `albuns_do_artista` que recebe como parâmetro o nome de uma pessoa artista e em retorno deve exibir seus respectivos álbuns. Os resultados devem ser ordenados pelo nome do álbum em ordem alfabética;

10 - Crie uma FUNCTION chamada de `quantidade_musicas_no_historico` que exibe a quantidade de músicas que estão presentes atualmente no histórico de reprodução de uma pessoa usuária;

11 - Crie uma VIEW chamada `cancoes_premium` exibindo o nome e a quantidade de vezes que cada canção foi tocada por pessoas usuárias do plano familiar ou universitário. Os resultados devem estar agrupados pelo nome da canção e ordenados alfabeticamente.
