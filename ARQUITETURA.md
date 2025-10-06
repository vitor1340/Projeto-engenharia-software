# Documentação da Arquitetura - Conexão Vida

## 1. Escolhas Tecnológicas
- **Framework Back-end:** Django (Python). Escolhido por sua filosofia "baterias inclusas", que oferece um painel de administração (Admin Interface) pronto para uso. Isso acelera drasticamente o desenvolvimento dos requisitos do perfil Admin (`RF01`, `RF02`, `RF04`), permitindo focar na lógica de negócio principal.
- **Front-end:** HTML, CSS com Bootstrap. Uma escolha pragmática para construir uma interface limpa, responsiva e profissional sem a necessidade de um framework JavaScript complexo, mantendo o escopo do projeto controlável.
- **Banco de Dados:** PostgreSQL. Um sistema de banco de dados relacional poderoso e confiável, que se integra perfeitamente com o Django e é capaz de suportar o crescimento futuro da aplicação.

## 2. Projeto Arquitetural (C4 Model)

### Nível 1: Diagrama de Contexto
O diagrama de contexto mostra os dois tipos de usuários interagindo com o sistema "Conexão Vida". O `Admin` gerencia o conteúdo do sistema, enquanto o `Visitante` (doador) consome essa informação através de um navegador web.


### Nível 2: Diagrama de Contêineres
O sistema é uma **Aplicação Web Monolítica** construída com Django. Ela é composta por:
1.  **Servidor Web (Web Application):** A aplicação Django que executa em um servidor. Ela é responsável por renderizar as páginas HTML (front-end), processar a lógica de negócio (API interna), autenticar os Admins e se comunicar com o banco de dados.
2.  **Banco de Dados (Database):** Uma instância do PostgreSQL que armazena todos os dados da aplicação: usuários admin, centros de coleta e apelos.

O navegador do usuário (tanto do Admin quanto do Visitante) faz requisições HTTP para a Aplicação Web, que devolve as páginas já renderizadas.


## 3. Justificativa do Modelo
A arquitetura monolítica tradicional com Django é a mais eficiente para este projeto. Ela simplifica o desenvolvimento e a implantação, já que front-end e back-end são gerenciados no mesmo lugar. A principal vantagem é o Django Admin, que fornece uma interface segura e pronta para a administração dos dados, atendendo a quase metade dos requisitos funcionais com esforço mínimo de desenvolvimento.
