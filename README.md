## Testes de API com MockMvc e RestAssured

Visão geral sobre testes de API
Contextualização
- Testes de API são testes que executamos diretamente nos endpoints da nossa aplicação, de forma a validar comportamentos inesperados, evitando que usuários e aplicações desta API recebam resultados inesperados.
- Por meio dos testes é possível avaliar critérios da API como funcionalidade, desempenho, confiabilidade e segurança.
- Testes de API são um tipo de teste de integração
- Lembrando, que os testes de integração são chamados de testes em caixa preta, ou seja, baseado nos requisitos, de forma que especificamos as entradas e saídas da nossa API, buscando cobrir os cenários importantes.
- Vamos aprofundar nos testes de API usando duas ferramentas: MockMvc e Rest Assured
MockMvc
- MockMvc fornece suporte para testarmos nossa aplicação spring, encapsulando todos os beans necessários para testar a camada web;
- Amplamente usado para fazer o teste de integração;
- O teste de integração desempenha um papel importante no ciclo de vida de uma aplicação, verificando o comportamento de ponta a ponta de um sistema;
Rest Assured
- REST Assured é uma biblioteca usada para automatizar testes de API em aplicações, permitindo testar e validar serviços REST de uma forma simples.

- Documentação oficial 
https://rest-assured.io/

Exemplo básico utilização REST Assured
- Para este exemplo, vamos considerar uma API para consultar partidas entre dois times, conforme a Figura (abaixo):

![image](https://github.com/JonasRF/DSCommerce-RestAssured/assets/77034798/4ddb47c8-6e22-4e97-be6a-4f72fad150b0)

- Considere que o endpoint para consultar esta partida seja http://localhost:8080/events?id=390 
- Desta forma, utilizando o Rest Assured podemos fazer uma requisição para o endpoint /events e consultar pelo evento de id = 390. Em seguida, podemos acessar os valores retornados no Json e validá-los.
- Na Figura (abaixo), temos um teste em que dada à URI, deve retornar 200 (OK) e em seguida obter o corpo da resposta e validar se o valor leagueId corresponde a 35.

![image](https://github.com/JonasRF/DSCommerce-RestAssured/assets/77034798/51e7bfa6-b56c-47dc-ac09-314b2e976457)

##Recursos importantes

Dependência -Rest Assured-

```
<dependency>
	<groupId>io.rest-assured</groupId>
	<artifactId>rest-assured</artifactId>
	<scope>test</scope>
</dependency>
```

Dependência para permitir criar um objeto JSON a partir de um Map

```
<dependency>
	<groupId>com.googlecode.json-simple</groupId>
	<artifactId>json-simple</artifactId>
	<version>1.1.1</version>
</dependency>
```


