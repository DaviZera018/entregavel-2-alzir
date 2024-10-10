# Projeto de Operações Matemáticas

Este projeto consiste em uma aplicação front-end que consome uma API desenvolvida em Java usando Spring Boot. A API oferece várias operações matemáticas, incluindo troca de valores de variáveis, somador, cálculo de Fibonacci e verificação de números primos.

## Estrutura do Projeto

```
/projeto-operacoes
├── /frontend
│   ├── index.html
│   ├── style.css
│   └── script.js
└── /backend
    ├── src
    │   ├── main
    │   │   ├── java
    │   │   └── resources
    └── pom.xml
```

## Front-end

### Tecnologias Utilizadas

- HTML
- CSS
- JavaScript

### Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/seuusuario/projeto-operacoes.git
   cd projeto-operacoes/frontend
   ```

2. Abra o arquivo `index.html` em um navegador para visualizar a aplicação.

### Funcionalidades

- **Troca de Valores**: Permite ao usuário trocar os valores de duas variáveis.
- **Somador**: Realiza a soma de dois números.
- **Fibonacci**: Calcula o enésimo número de Fibonacci.
- **Primalidade**: Verifica se um número é primo.

### Exemplo de Uso

Após abrir o `index.html`, o usuário poderá inserir os valores nos campos apropriados e clicar nos botões correspondentes para realizar as operações.

### Conexão com a API

A aplicação utiliza `fetch` para se comunicar com a API. As URLs para as operações são as seguintes:

- Troca de Valores: `POST /api/troca`
- Somador: `POST /api/soma`
- Fibonacci: `GET /api/fibonacci/{n}`
- Verificar Primo: `GET /api/primo/{n}`

## Backend

### Tecnologias Utilizadas

- Java
- Spring Boot

### Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/seuusuario/projeto-operacoes.git
   cd projeto-operacoes/backend
   ```

2. Navegue até o diretório do projeto e execute:
   ```bash
   ./mvnw spring-boot:run
   ```

### Funcionalidades da API

- **Troca de Valores**: Endpoint para trocar os valores de duas variáveis.
- **Somador**: Endpoint que recebe dois números e retorna a soma.
- **Fibonacci**: Endpoint que retorna o enésimo número de Fibonacci.
- **Primalidade**: Endpoint que verifica se um número é primo.

### Endpoints

- **Troca de Valores**
  - **Método**: POST
  - **URL**: `/api/troca`
  - **Corpo**: `{ "a": valor1, "b": valor2 }`
  - **Resposta**: `{ "a": valor2, "b": valor1 }`

- **Somador**
  - **Método**: POST
  - **URL**: `/api/soma`
  - **Corpo**: `{ "a": valor1, "b": valor2 }`
  - **Resposta**: `{ "resultado": soma }`

- **Fibonacci**
  - **Método**: GET
  - **URL**: `/api/fibonacci/{n}`
  - **Resposta**: `{ "resultado": fibonacci }`

- **Verificar Primo**
  - **Método**: GET
  - **URL**: `/api/primo/{n}`
  - **Resposta**: `{ "primo": true/false }`

### Executando Testes

Para executar os testes, use o comando:

```bash
./mvnw test
```
