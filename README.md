📦 Projeto LeiloesTDSat - Sistema de Gerenciamento de Leilões
Este projeto consiste em um sistema Java desktop para a gestão de itens de leilão, integrando uma interface gráfica Swing com persistência de dados em banco de dados MySQL.
🚀 Implementações da Atividade 2 (Revisadas)
O sistema foi estruturado seguindo o padrão DAO (Data Access Object), garantindo uma separação clara entre a interface e a lógica de persistência.
1. Robustez e Tratamento de Erros Multi-Camadas
·	Validação de Interface (VIEW): Implementação de blocos try-catch específicos para NumberFormatException no cadastro, garantindo que o campo "Valor" aceite apenas números e forneça feedback claro via JOptionPane.
·	Persistência Segura (DAO): Todos os métodos de banco de dados (cadastrar, listar, vender) possuem tratamento de exceções para capturar falhas de conexão ou erros de SQL.
·	Gestão de Recursos: Uso rigoroso de blocos finally para o fechamento de Connections, PreparedStatements e ResultSets, prevenindo vazamentos de memória e sobrecarga do servidor MySQL.
2. Experiência do Usuário (UX/UI)
·	Centralização Dinâmica: Todas as telas (cadastroVIEW, listagemVIEW) utilizam setLocationRelativeTo(null), iniciando centralizadas no monitor do usuário.
·	Feedback Visual: Implementação de mensagens de confirmação de sucesso e alertas de erro para todas as operações críticas.
·	Navegação Fluida: O sistema gerencia o ciclo de vida das janelas, limpando formulários após o cadastro e atualizando tabelas automaticamente ao carregar a lista.
3. Configurações Técnicas
·	Conexão JDBC: Classe conectaDAO configurada para ambiente local com parâmetros de segurança e suporte a driver MySQL Connector 8.0.
·	Banco de Dados: O projeto acompanha o script UC11.sql para criação da estrutura necessária.
·	Bibliotecas: Driver JDBC incluído na pasta biblioteca para garantir portabilidade.
📂 Estrutura de Pastas Principal
·	src/: Código-fonte Java (Classes DAO, DTO e VIEW).
·	lib/ ou biblioteca/: Drivers e dependências externas.
·	dist/javadoc/: Documentação técnica gerada automaticamente.
·	UC11.sql: Script de banco de dados.

Desenvolvido como parte dos requisitos da Atividade 2 - Unidade Curricular de Codificação Java.
