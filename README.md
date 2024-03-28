## Testes de API com MockMvc e RestAssured

Visão geral sobre testes de API
Contextualização
  -- Testes de API são testes que executamos diretamente nos endpoints da nossa aplicação, de forma a validar comportamentos inesperados, evitando que usuários e aplicações desta API recebam resultados inesperados.
  -- Por meio dos testes é possível avaliar critérios da API como funcionalidade, desempenho, confiabilidade e segurança.
Testes de API são um tipo de teste de integração
Lembrando, que os testes de integração são chamados de testes em caixa preta, ou seja, baseado nos requisitos, de forma que especificamos as entradas e saídas da nossa API, buscando cobrir os cenários importantes.
Vamos aprofundar nos testes de API usando duas ferramentas: MockMvc e Rest Assured
MockMvc
MockMvc fornece suporte para testarmos nossa aplicação spring, encapsulando todos os beans necessários para testar a camada web;
Amplamente usado para fazer o teste de integração;
O teste de integração desempenha um papel importante no ciclo de vida de uma aplicação, verificando o comportamento de ponta a ponta de um sistema;
Rest Assured
REST Assured é uma biblioteca usada para automatizar testes de API em aplicações, permitindo testar e validar serviços REST de uma forma simples.
