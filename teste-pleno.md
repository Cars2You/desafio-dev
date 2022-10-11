
<p align="center">
  <img src="https://storage.googleapis.com/arquivos-a2y/arquivos/2020_04_22/JP85PSytO7p78cUILy9O.png" width="320" alt="Nest Logo" />
</p>

## Seja Bem vindo à Cars2You!

Estamos felizes de ter você no nosso processo seletivo para Equipe de Desenvolvimento!

Neste processo, vamos analisar seu conhecimento sobre APIs Rest, Javascript (e/ou Typescript) e Git!

### Como enviar o desafio
Crie um repositório público no [Github](https://github.com/). Assim que finalizar seu desafio, envie o link do repositório para sua recrutadora.

Lembre-se que estamos analisando seu conhecimento Git também, então utilize [Commits Semânticos](https://blog.geekhunter.com.br/o-que-e-commit-e-como-usar-commits-semanticos/) no processo de desenvolvimento do desafio.

ex: 
- Caso esteja desenvolvendo o endpoint de Veículo, crie uma branch chamada `feature/endpoint-veiculos`.
- Faça os commits semânticos nela, ex: `feat(Veículo): Criado endpoint GET de veiculos`.
- Quando finalizar, realize o merge para a branch `main`

### Dúvidas sobre o desafio

Caso tenha alguma dúvida sobre o desafio, [abra uma issue](https://github.com/cars2you/desafio-devpleno/issues) neste repositório e alguém da nossa equipe vai te ajudar! Utilizamos as issues para que cada dúvida possa servir de ajuda para o próximo! 


#### A seguir, está seu desafio, boa sorte! 


## DESAFIO

**Resumo:**

- Criar um Banco de dados MySQL
- Criar uma api para consumir o banco de dados Mysql utilizando TypeORM ou Prisma como ORM

**Diferenciais:**

Você deverá usar o [`nest.js`](https://docs.nestjs.com/) como servidor e o [`typeORM`](https://typeorm.io/) como ORM. Você poderá usar ou não typescript se seguir esta opção. Fica ao seu critério.

### Instruções:

## 1. Criar um banco MySQL
### 1.1. Criar a tabela:


#### Veiculo
| coluna      | tipo    | descrição                |
|-------------|---------|--------------------------|
| id          | int     | Chave primária da tabela |
| idCategoria | int     | id da Categoria (fk) |
| marca       | varchar | Marca do Veículo         |
| modelo      | varchar | Modelo do Veículo        |
| ano         | int     | Ano do Veículo           |
| peso        | float   | Peso do Veículo          |
| cor         | varchar | Cor do Veículo           |
| status      | int     | 0 - Inativo, 1 - Ativo   |

#### Categorias
| coluna      | tipo    | descrição                |
|-------------|---------|--------------------------|
| id          | int     | Chave primária da tabela |
| nome        | varchar | Nome da Categoria        |

<br>

### 2. Desenvolver uma API Restful:

	- Veiculo
	
	[GET] 	 /veiculo 		- Lista todos os Veículos
	[GET] 	 /veiculo/:id 	- Busca um Veículo por id
	[POST] 	 /veiculo 		- Cria um Veículo
	[PATCH]  /veiculo/:id 	- Edita um Veículo
	[DELETE] /veiculo/:id	- Deleta um Veículo (e seu estoque)

    - Categorias

    [GET] 	 /categorias 		- Lista todas as Categorias
    [GET] 	 /categorias/:id 	- Busca uma Categoria por id
    [POST] 	 /categorias 		- Cria uma Categoria
    [PATCH]  /categorias/:id 	- Edita uma Categoria
    [DELETE] /categorias/:id	- Deleta uma Categoria (deve atualizar o veiculo setando idCategoria como NULL para veiculos que utilizam essa categoria)

# Boa sorte!

-- Equipe Cars2You
