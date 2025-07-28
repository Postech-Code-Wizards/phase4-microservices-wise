# 🧠 Phase 4 - Wise Microservices

Este repositório contém o projeto final da Fase 4 do Pós-Tech em Arquitetura de Software, que implementa uma arquitetura de microsserviços para gerenciamento de pedidos em um ambiente distribuído, utilizando Docker, Quarkus e mensageria com RabbitMQ.

---

## 📦 Microserviços

O projeto é composto pelos seguintes serviços:
| Serviço               | Descrição                               |
|-----------------------|-------------------------------------------|
| `wise-client-service` | Gerenciamento de clientes                 |
| `wise-product-service`| Gerenciamento de produtos                 |
| `wise-stock-service`  | Controle de estoque                      |
| `wise-order-service`  | Gerenciamento de pedidos                 |
| `wise-payment`        | Processamento de pagamentos              |
| `wise-order-receiver` | Orquestrador de pedidos via fila RabbitMQ |

---

## 🚀 Tecnologias Utilizadas

- Java + Quarkus + SpringBoot
- PostgreSQL
- H2 para testes
- RabbitMQ  
- Docker + Docker Compose  
- JaCoCo para cobertura de testes  
- Mockito + JUnit para testes unitários  
- Git Submodules  

---

## ▶️ Como rodar o projeto

1. Clone o repositório:
   ```bash
   git clone https://github.com/Postech-Code-Wizards/phase4-microservices-wise.git
   cd phase4-microservices-wise
    ```
2. Atualize os submódulos:
   ```bash
   git submodule update --init --recursive
    ```
3. Suba todos os serviços com Docker:
   ```bash
   docker compose up --build
   ```
4. Acesse os serviços nas portas configuradas no `docker-compose.yml`, utilizando a [coleção do Postman](https://postech-code-wizards.postman.co/workspace/FoodWise-Backend~6e8c7ccc-d1f8-42e7-bd4d-899bd31909e7/collection/39830207-535c2390-f87a-47b1-a52e-acafc25e4169?action=share&creator=39830207) para testar os endpoints.
   
---

## 🧪 Executando os testes e cobertura com JaCoCo

Cada microserviço possui testes com cobertura via **JaCoCo**.
Nesse repositório está uma pasta com todos os arquivos.

### ✅ Rodando os testes

Para gerar o relatório de cobertura de testes em um dos serviços (exemplo: `wise-order-service`):

```bash
cd wise-order-service
./mvnw clean verify
```

📊 Acessando o relatório
O relatório será gerado em:
```bash
target/site/jacoco/index.html
```

⚠️ O microserviço wise-client-service utiliza Quarkus, por isso configuramos comando diferente para gerar corretamente os relatórios de cobertura de testes incluindo o Controller.

Para esse serviço, utilize:

```bash
./mvnw clean test jacoco:report
```

O relatório será gerado em:
```bash
target/jacoco-report/index.html
```

Abra este arquivo no seu navegador para visualizar a cobertura de código! 💡

---

## 👥 Equipe
| RM         | Nome                     |
|------------|--------------------------|
| RM360641   | Anderson Donnarumma      |
| RM360133   | João Marcos              |
| RM360421   | Isabela Caovila Baldim   |
| RM360259   | Mateus Bonet             |
| RM360490   | Vitor Hugo de Souza      |

---
## 🎥 Demonstração
👉 Assista à demo do sistema:
🔗 [Link para o vídeo no Google Drive](https://drive.google.com/file/d/16wQxJu1O8ynWntb4XSq0sftnV6QJT2cR/view)
