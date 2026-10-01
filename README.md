# API Gateway

## Descrição

Gateway de entrada para os microsserviços da aplicação, centralizando o roteamento das requisições, a autenticação baseada em JWT e a documentação agregada das APIs.

## Funcionalidades

- Roteamento para os serviços de produto, pedido e inventário
- Validação de tokens JWT emitidos pelo Keycloak
- Agregação da documentação OpenAPI dos serviços
- Circuit breaker com rota de fallback para indisponibilidade dos serviços
- Retry, time limiter e métricas de observabilidade
- Exposição de endpoints de monitoramento via Actuator

## Tecnologias

- **Spring Framework** — Injeção de Dependências, Beans e Configurações
- **Spring Boot** — Autoconfiguração, Starter POMs e Actuator
- **Spring Cloud Gateway** — Roteamento e filtros das requisições
- **Spring Security OAuth2 Resource Server** — Validação de tokens JWT
- **Resilience4j** — Circuit breaker, retry e time limiter
- **Springdoc OpenAPI** — Documentação e agregação das APIs
- **Keycloak** — Provedor de identidade e autorização
- **Prometheus, Grafana, Loki e Tempo** — Métricas, logs e tracing

## Pré-requisitos

- Java Development Kit (JDK) 21 ou mais recente
- Maven
- Docker
- Keycloak configurado na porta `8181`
- Serviços de produto, pedido e inventário disponíveis nas portas configuradas

## Execução

Para iniciar a infraestrutura de observabilidade e o Keycloak:

```bash
docker compose up -d
```

Para executar o gateway:

```bash
./mvnw spring-boot:run
```

O gateway ficará disponível em `http://localhost:9000`. A interface Swagger pode ser acessada em `http://localhost:9000/swagger-ui.html`.
