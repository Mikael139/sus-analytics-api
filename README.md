# SUS Predict - API de Análise e Previsão

## Sobre o Projeto
O SUS Predict é uma plataforma de inteligência preditiva voltada para a gestão pública da saúde. A solução tem como objetivo transformar grandes volumes de dados públicos do Sistema Único de Saúde (SUS) em informações estratégicas para planejamento, permitindo antecipar cenários críticos antes que eles ocorram. O projeto se insere na área de HealthTech, utilizando tecnologia para melhorar serviços de saúde, gestão hospitalar e acesso a cuidados médicos.

## Problemas que Resolvemos
A plataforma foi desenvolvida para ajudar a mitigar grandes desafios do sistema público de saúde:
* **Sobrecarga hospitalar:** Hospitais frequentemente operam próximos ou acima de sua capacidade máxima de atendimento, gerando atrasos no atendimento e sobrecarga dos profissionais da saúde.
* **Falta de previsibilidade de insumos:** A dificuldade em prever a demanda por medicamentos muitas vezes resulta em escassez de remédios essenciais ou exige compras emergenciais com custos mais elevados.
* **Pressão financeira:** O aumento constante da demanda por serviços médicos, aliado ao crescimento dos custos hospitalares, exerce forte pressão sobre os orçamentos de saúde de municípios e estados.

## Principais Funcionalidades
* Previsão da ocupação de leitos hospitalares com base em dados históricos e sazonalidade.
* Identificação antecipada de risco de superlotação hospitalar em determinadas regiões.
* Análise de demanda por medicamentos e insumos hospitalares.
* Monitoramento do consumo de medicamentos no sistema de saúde.
* Projeção de gastos hospitalares e pressão sobre orçamentos municipais.

## Arquitetura e Segurança
O projeto utiliza uma arquitetura baseada em microsserviços, na qual diferentes componentes da plataforma (como coleta de dados, processamento e análise preditiva) funcionam de forma independente. A utilização de infraestrutura em nuvem facilita o armazenamento e processamento de grandes volumes de dados. A segurança segue o conceito de Security by Design, no qual mecanismos como criptografia de dados, autenticação segura e controle de acesso são incorporados desde o início para reduzir riscos de ataques cibernéticos.

---

## Ferramentas Utilizadas
De acordo com o arquivo de configuração `pom.xml` do projeto, a API foi construída utilizando as seguintes tecnologias:

* **Linguagem:** Java 21
* **Framework Principal:** Spring Boot (versão 4.0.3)
* **Web & APIs:** Spring Boot Starter Web
* **Persistência de Dados:** Spring Boot Starter Data JPA
* **Banco de Dados:** H2 Database (banco em memória para desenvolvimento/testes) e PostgreeSQL
* **Documentação:** Springdoc OpenAPI UI (versão 3.0.2) para geração automática do Swagger
* **Produtividade:** Lombok
* **Testes:** Spring Boot Starter Test e Maven Surefire Plugin (versão 3.5.4)
* **Gerenciador de Dependências e Build:** Maven

## Como Instalar e Executar

**Pré-requisitos:**
* Ter o **Java 21 (JDK)** instalado.
* Ter o **Maven** instalado e configurado nas variáveis de ambiente do sistema.

**Passo a passo:**

1. **Acesse o repositório:** Navegue pelo seu terminal até o diretório raiz do projeto onde o arquivo `pom.xml` da `sus-analytics-api` está localizado.
2. **Baixe as dependências e compile o projeto:** Execute o comando abaixo para que o Maven resolva todas as dependências e construa a aplicação:
   ```bash
   mvn clean install
3. **Inicie a aplicação:** Suba o servidor embutido do Spring Boot executando o seguinte comando:
   ```bash
   mvn spring-boot:run
4. **Teste a API:**
- A aplicação estará disponível por padrão na porta **8080**.
- Para visualizar e testar os endpoints através da interface gráfica do Swagger, acesse em seu navegador: http://localhost:8080/swagger-ui.html.
