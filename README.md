# TaPago
API do projeto TaPago - Controle de Gastos Pessoais

## Tarefas

- [] CRUD de Categorias
- [] CRUD de Movimentos
- [] CRUD de Usuários
- [] Dashboard

## Documentação API

### Endpoint
- [Listar Todas as Categorias](#listar-todas-as-categorias)
- [Cadastrar Categorias](#cadastrar-categoria)
- [Detalhes da Categoria](#detalhes-da-categoria)
- [Apagar Categoria](#apagar-categoria)
- [Atualizar Categoria](#atualizar-categoria)

---

### Listar todas as Categorias

`GET` /categoria

Retorna um array com todas as categorias cadastradas

#### Exemplo de Resposta

```
[
    {
        "id": 1,
        "nome": "Alimentação",
        "icone": "fast-food"
    }
]
```

#### Código de Status

|código|descrição|
|------|---------|
|200|Os dados das categorias foram retornados com sucesso|
|401|Acesso negado. Você deve se autenticar|

---

### Cadastrar Categoria

`POST` /categoria

Cria uma nova categoria com os dados enviados no corpo da requisição.

#### Corpo da Requisição

|campo|tipo|obrigatório|descrição|
|-----|----|:-----------:|---------|
|nome|string|✅|Um nome curto para a categoria.|
|icone|string|❌|O nome do ícone de acordo com a biblioteca Material Icons|

```js
{
    "nome": "Alimentação"
    "icone": "fast-food"
}
```

#### Corpo da Resposta 
|código|descrição|
|------|---------|
|201|Categoria cadastrada com sucesso|
|400|Dados enviados são inválidos. Verifique o corpo da requisição|
|401|Acesso negado. Você deve se autenticar|

---

### Detalhes da Categoria

`GET` /categoria/`{id}`

Retorna os detalhes da categoria com o `id` informado como parâmetro de path. 

#### Exemplo de Resposta

```js
// requisição para /categoria/1
[
    {
        "id": 1,
        "nome": "Alimentação",
        "icone": "fast-food"
    }
]
```

#### Códigos de Status

|código|descrição|
|------|---------|
|200|Os dados das categorias foram retornados com sucesso|
|401|Acesso negado. Você deve se autenticar|
|404|Não existe categoria com o `id` informado|

---

### Apagar Categoria

`DELETE` /categoria/`{id}`

Apaga a categoria com o `id` especificado no parâmetro de path.

#### Códigos de Status

|código|descrição|
|------|---------|
|204|Categoria foi apagada com sucesso|
|401|Acesso negado. Você deve se autenticar|
|404|Não existe categoria com o `id` informado|

---

### Atualizar Categoria

`PUT` /categoria/`{id}`

Alteração dos dados da categoria especificada com o `id`, utilizando as informações enviadas no corpo da requisição.

#### Corpo da Requisição

|campo|tipo|obrigatório|descrição|
|-----|----|:-----------:|---------|
|nome|string|✅|Um nome curto para a categoria.|
|icone|string|✅|O nome do ícone de acordo com a biblioteca Material Icons|

```js
{
    "nome": "Alimentação"
    "icone": "fast-food"
}
```

#### Exemplo de Resposta

```js
[
    {
        "id": 1,
        "nome": "Alimentação",
        "icone": "fast-food"
    }
]
```

#### Códigos de Status

|código|descrição|
|------|---------|
|200|Os dados das categorias foram retornados com sucesso|
|400|Dados enviados são inválidos. Verifique o corpo da requisição|
|401|Acesso negado. Você deve se autenticar|
|404|Não existe categoria com o `id` informado|

---






