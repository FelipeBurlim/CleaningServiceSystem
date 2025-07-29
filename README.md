Este projeto visa desenvolver um sistema em Python para uma prestadora de serviços de limpeza, com o objetivo de gerenciar dados de faxineiros(as), clientes e os serviços contratados. O sistema será construído com base em princípios de programação estruturada, utilizando funções para cada operação e evitando o uso de variáveis globais. A persistência dos dados é um requisito chave, o que significa que todas as informações serão armazenadas em arquivos de texto dedicados para cada tipo de entidade (Faxineiros, Clientes, Serviços), e os relatórios gerados também serão persistidos em arquivos.

Funcionalidades Principais:
O sistema operará através de um Menu Principal que direciona o usuário para submenus específicos para cada entidade, além de um submenu para relatórios.

1. Submenus de Gerenciamento (Faxineiros, Clientes, Serviços):
Cada um desses submenus oferecerá as seguintes operações CRUD (Create, Read, Update, Delete):
Listar todos: Exibir todos os registros da entidade.
Listar um: Buscar e exibir os dados de um registro específico, geralmente por sua chave primária.
Incluir: Adicionar um novo registro. É crucial que o sistema não permita a inclusão de registros com chaves duplicadas (CPF para faxineiros e clientes, e a combinação de CPF do faxineiro, CPF do cliente e data para serviços).
Alterar: Modificar os dados de um registro existente.
Excluir: Remover um registro, com uma confirmação prévia para evitar exclusões acidentais.

2. Submenu de Relatórios:
Este submenu será dedicado à geração de relatórios específicos, que também serão persistidos em arquivos de texto:
a) Clientes que contrataram determinado(a) faxineiro(a) entre datas X e Y: O usuário fornecerá o CPF do(a) faxineiro(a) e um período de datas, e o relatório exibirá o nome, e-mails e telefones dos clientes que contrataram serviços desse(a) faxineiro(a) no período.
b) Serviços contratados para uma data específica: O usuário informará uma data, e o relatório mostrará os dados de todos os serviços realizados nessa data, incluindo os nomes do(a) faxineiro(a) e do(a) cliente envolvidos.
c) Serviços realizados por determinado(a) faxineiro(a): O usuário fornecerá o CPF do(a) faxineiro(a), e o relatório listará todos os serviços que ele(a) realizou.
