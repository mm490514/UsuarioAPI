# Documentação da API

Este é um modelo simples de API em PHP que segue um design RESTful para lidar com operações relacionadas a usuários. A API utiliza o framework Slim para roteamento e depende do Composer para carregar automaticamente as classes.

## Instalação

1. Clone o repositório:

   ```bash
   git clone https://github.com/seu/repo.git
   ```

2. Instale as dependências usando o Composer:

   ```bash
   composer install
   ```

3. Configure seu servidor web para apontar para o diretório `public`.

## Uso

### Endpoint

O endpoint da API segue o padrão: `/api/{recurso}/{id}`.

### Métodos

- **GET**: Recupera um ou mais recursos
- **POST**: Cria um novo recurso
- **PUT/PATCH**: Atualiza um recurso
- **DELETE**: Exclui um recurso

### Exemplos

#### Recuperar Usuário

```http
GET /api/usuarios/1
```

#### Criar Usuário

```http
POST /api/usuarios
```

Inclua um corpo JSON:

```json
{
    "nome": "Fulano de Tal",
    "email": "fulano@example.com"
}
```

#### Atualizar Usuário

```http
PUT /api/usuarios/1
```

Inclua um corpo JSON:

```json
{
    "nome": "Nome Atualizado"
}
```

#### Excluir Usuário

```http
DELETE /api/usuarios/1
```

### Formato de Resposta

A API retorna respostas no formato JSON.

#### Resposta de Sucesso

```json
{
    "status": "sucesso",
    "data": { ... }
}
```

#### Resposta de Erro

```json
{
    "status": "erro",
    "data": "Mensagem de erro"
}
```

## Tratamento de Erros

- Solicitações bem-sucedidas retornam o status `200 OK`.
- Se ocorrer um erro, a API responde com o status `404 Not Found` e uma mensagem de erro.

## Dependências

- Slim Framework: [https://www.slimframework.com/](https://www.slimframework.com/)
- Composer: [https://getcomposer.org/](https://getcomposer.org/)

## Nota

Este é um modelo básico, e você deve personalizá-lo de acordo com seus requisitos específicos. Certifique-se de implementar medidas de segurança adequadas e validar a entrada do usuário para evitar vulnerabilidades de segurança.
