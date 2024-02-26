# TaPago
API do projeto TaPago - Controle de Gastos Pessoais

## Tarefas

- [] CRUD de Categorias
- [] CRUD de Movimentos
- [] CRUD de Usuários
- [] Dashboard

## Documentação API

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
|200|Os dados das categorias foram retornados com sucesso
401|Acesso negado. Você deve se autenticar
