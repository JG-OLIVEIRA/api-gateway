<h1 align="center">API gateway</h1>

<p>A API Gateway é uma parte crítica da arquitetura de microservices, fornecendo um ponto centralizado para gerenciar solicitações de API e direcioná-las para os serviços. A API Gateway oferece benefícios como simplificação da arquitetura, aumento da segurança e melhoria no desempenho. Leia o documento para saber mais sobre a importância da API Gateway na arquitetura de microservices.<p>

## Instalação

1. Clone o projeto
```bash
git clone https://github.com/JG-OLIVEIRA/api-gateway
```
2. Vá até à pasta raiz do projeto
```bash
cd api-gateway
```
3. Use `mvn package` para gerar a pasta `target` contendo o execultável da aplicação
```bash
mvn package
```
4. Agora rode a aplicação que vai estar disponível no url http://localhost:8080

```java
package com.programming.techie.apigateway;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class ApiGatewayApplication {
    public static void main(String[] args) {
        SpringApplication.run(ApiGatewayApplication.class, args);
    }
}
```