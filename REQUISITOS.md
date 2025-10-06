# Requisitos do Projeto: Conexão Vida

## Perfis de Usuário
- **Admin (Funcionário do Hemocentro):** Usuário com permissão para gerenciar apelos e informações dos centros de coleta.
- **Visitante (Doador em Potencial):** Usuário público que acessa o site para visualizar informações.

## Requisitos Funcionais (RF)
- **RF01:** O sistema deve ter uma área de login segura para usuários Admin.
- **RF02:** Um Admin logado deve poder criar, editar, ativar/desativar e excluir um apelo por tipo sanguíneo.
- **RF03:** Um apelo deve conter o tipo de sangue, nível de urgência (crítico, alerta, estável) e o centro de coleta associado.
- **RF04:** Um Admin logado deve poder gerenciar as informações dos centros de coleta (nome, endereço, horário de funcionamento).
- **RF05:** O Visitante deve poder visualizar em uma página principal o feed de apelos ativos, ordenados por urgência e data.
- **RF06:** O Visitante deve poder visualizar uma página com a lista de todos os centros de coleta cadastrados e seus detalhes.

## Requisitos Não Funcionais (RNF)
- **RNF01:** A plataforma deve ser responsiva.
- **RNF02:** O painel administrativo deve ser protegido contra acesso não autorizado.
- **RNF03:** O back-end será desenvolvido em Python com o framework Django, aproveitando sua interface de administração nativa para acelerar o desenvolvimento.
- **RNF04:** O front-end será desenvolvido com HTML/CSS e Bootstrap para garantir uma interface limpa e responsiva rapidamente.
- **RNF05:** O banco de dados utilizado será o PostgreSQL.
https://drive.google.com/file/d/1_uKNwq2AF_n8BcI47nzUI2OmjqR8S9Lj/view?usp=sharing (LINK DO DIAGRAMA)
