# API, REST and RESTFUL

- Cliente (Cliente)
- Garçon (pedido, levar seus pedidos para cozinha) (API)
- Cozinha (Server)

## API

Acronimo de Aplication Programming Interface (Interface de Programação de Aplicações) é basicamente um conjunto de rotinas e padrões estabelecidos por uma aplicação, para que outras aplicações possam utilizar as funcionalidades desta aplicação.ss

- Responsavel por estabelecer comunicação entre diferentes serviços.
- Meio de campo entre as tecnologias.
- Intermediador para troca de informação.

## REST

Um acrónimo para Representational State Transfer (Transferencia de Estado Representativo).

A transferencia de dados, geralmente usando o protocolo HTTP.

O Rest, delimita algumas obrigações nessas transferências de dados.

Resources seria então, uma entidade, um objecto.

### 6 NECESSIDADES (constraints) para ser RESTful

- _Client-server_: Separação do cliente e do armazenamento de dados (servidor), dessa forma, poderemos ter uma portabilidade do nosso sistema, usando o React para Web e React Native para o smartphone, por exemplo.

- _Stateless_: Cada requisição que o cliente faz para o servidor, deverá conter todas as informações necessárias para o servidor entender e responder (RESPONSE) a requisição (REQUEST).

  - **Exemplo**: A sessão do usuário deverá ser enviada em todas as requisições, para saber se aquele uauário está autenticado e apto a usar os serviços, e o servidor não pode lembrar que o cliente foi autenticado na requisição anterior. Nos nossos cursos, temos por padrão usar tokens para as comunicações.

- _Cacheable_: As respostas para uma requisição, deverão ser explicitas ao dizer se aquela requisição, pode ou não ser cacheada pelo cliente.

- _Layered System_: O cliente acessa a um endpoint, sem precisar saber da complexidade, de quais passos estão sendo necessários para o servidor responder a requisição, ou quais outras camadas o servidor estará lidando, para que a requisição seja respondida.

- _Code on demand (optional)_: Dá a possibilidade da nossa aplicação pegar codigos, como o javascript, por exemplo, e executar no cliente;

## RESTFUL

RESTful, é a plicação dos padrões REST.

## BOAS PRÁTICAS

- Utilizar verbos HTTP para nossas requisições.
- Utilizar plural ou singular na criação dos endpoits? _NÃO IMPORTA!_ use um padrão!!
- Não deixa barra no final do endpoint
- Nunca deixe o cliente sem resposta! (_Exemplo_: **200 OK**)

### VERBOS HTTP

- GET: Receber dados de um Resource.
- POST: Enviar dados ou informações para serem processados por um Resource.
- PUT: Actualizar dados de um Resource.
- DELETE: Deletar um Resource.

### STATUS DAS RESPOSTAS

- 1xx: Informação
- 2xx: Sucesso
  - 200: OK
  - 201: CREATED
  - 204: Não tem conteúdo PUT POST DELETE
- 3xx: Redirection
- 4xx: Client Error
  - 400: Bad Request
  - 404: Not Found
- 5xx: Server Error
  - 500: Internal Server Error

### SOME NOTES ASIDE

- Criamos o projecto: `yarn init -y` com package `JSON`
- Criamos o servidor: `yarn add express`
- Corremos o servidor: `node server.js`
