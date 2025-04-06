# Projeto-Desenvolvimento Desktop
Nome Integrantes:

Antonio Tiago Zaneratto R.A: 24000696 

Flavio Perussi Bertão dos Reis RA: 24001465 

João Pedro Dutra da Silva RA: 24000990        

Laís de Oliveira Lavras RA: 1012023200359 

Maicon Bruno Corrêa da Silva R.A: 24000795
________________________________________________________________________________________________________________________________________________________________________________________________________________________________________
Passo a Passo 

## 📘 Guia de Uso Técnico – Projeto Controle de Estoque (Java + MySQL)

Este guia descreve o processo de **edição, execução e testes** do sistema **Controle de Estoque**, desenvolvido em Java com banco de dados MySQL, utilizando o ambiente de desenvolvimento NetBeans e o WampServer como servidor local.

### ✅ **Pré-requisitos**
Antes de iniciar o uso e testes do sistema, verifique se os seguintes softwares estão instalados:

- MySQL Workbench (para edição do banco)
- WampServer (servidor local)
- NetBeans IDE (para executar o projeto Java)
- Navegador de internet com acesso ao phpMyAdmin

### 🔧 **Passo a Passo para Testar o Sistema**

#### **1. Edição do Banco de Dados**
- Abra o **MySQL Workbench**.
- Importe ou abra o arquivo `.sql` do banco **controle-estoque.sql**.
- Edite os campos necessários (ex: nomes de tabelas, valores iniciais, tipos de dados).
- Salve e exporte o arquivo atualizado, se necessário.

#### **2. Inicialização do Servidor Local**
- Execute o **WampServer**.
- Aguarde o ícone na bandeja do sistema ficar **verde** (indicando que os serviços Apache e MySQL estão ativos).
- Acesse o **phpMyAdmin** pelo navegador (geralmente: `http://localhost/phpmyadmin`).

#### **3. Importação do Banco no phpMyAdmin**
- No phpMyAdmin:
  - Clique em **Importar**.
  - Selecione o arquivo `controle-estoque.sql`.
  - Clique em **Executar**.
- Após importado, clique em **controle-estoque** na barra lateral para verificar as tabelas.

#### **4. Abertura do Projeto no NetBeans**
- Inicie o **NetBeans IDE**.
- Clique em **Abrir Projeto** e selecione a pasta do projeto **Controle de Estoque**.
- Aguarde o carregamento completo.

#### **5. Execução do Projeto**
- Com o projeto carregado, clique em **Executar Projeto (F6)**.
- A interface gráfica será exibida.
- Teste as **abas**, **formulários de cadastro**, e **consultas**.

#### **6. Testes de Integração**
- Após cadastrar ou atualizar informações no sistema:
  - Volte ao **phpMyAdmin**.
  - Verifique se os dados foram inseridos corretamente nas tabelas correspondentes.
  - Teste filtros, edições e exclusões na interface e veja se o banco está respondendo.

### 🛠️ Dicas Adicionais

- Se o projeto não conectar ao banco, verifique o arquivo de configuração de conexão (`Connection.java`, por exemplo).
- Confirme se o **usuário, senha e nome do banco** estão corretos.
- Certifique-se de que o MySQL está rodando no **mesmo host e porta** configurados no seu projeto Java.
________________________________________________________________________________________________________________________________________________________________________________________________________________________________________
O projeto foi utilizado alguns programas para realizar seu desenvolvimento assim como o WampServer como servidor local para realizar testes no projeto, oferecendo um ambiente integrado que inclui Apache, PHP e MySQL, essencial para simular o funcionamento da aplicação em condições similares às de um servidor de produção. Paralelamente, o phpMyAdmin foi empregado para o gerenciamento do banco de dados, facilitando tarefas como criação de tabelas, manipulação de dados e execução de consultas SQL. Essas ferramentas foram fundamentais para organizar e testar as informações no banco de dados, garantindo sua consistência e funcionalidade.
O desenvolvimento da aplicação foi realizado em Java, utilizando a IDE NetBeans, que oferece um conjunto robusto de recursos para programação orientada a objetos, como suporte a refatoração, depuração e integração com sistemas de controle de versão. O Maven, um importante framework de gerenciamento de dependências e automação de build, foi utilizado para estruturar o projeto, facilitar o gerenciamento de bibliotecas e garantir a portabilidade da aplicação. Durante o processo de desenvolvimento, foram aplicados conceitos de orientação a objetos, como criação de classes, definição de métodos e implementação de herança, promovendo uma arquitetura modular e reutilizável.
Se precisar de mais detalhes ou explicações sobre qualquer aspecto, é só dizer!
O desenvolvimento do projeto exigiu a instalação de diversas ferramentas essenciais. Aqui está um guia detalhado sobre como instalá-las, passo a passo, com os sites oficiais para download:
1. Instalação do NetBeans e JDK 24
•	Acesse o site oficial do NetBeans: https://netbeans.apache.org.
•	Acesse o site oficial do JDK: https://www.oracle.com/java/technologies/javase-jdk-downloads.html.
•	Passos para instalar o JDK 24: 
o	Faça o download da versão adequada para o seu sistema operacional (Windows, macOS ou Linux).
o	Execute o instalador e siga os passos fornecidos, como aceitar os termos de licença e selecionar o diretório de instalação.
o	Configure as variáveis de ambiente do sistema adicionando o caminho para o JDK, caso necessário, para que o compilador reconheça a instalação.
•	Passos para instalar o NetBeans: 
o	Baixe o instalador no site oficial e execute-o.
o	Durante a instalação, verifique se ele está configurado para usar o JDK previamente instalado.
o	Escolha o diretório de instalação e finalize o processo.
2. Instalação do MySQL Workbench
•	Acesse o site oficial: https://dev.mysql.com/downloads/workbench/.
•	Passos para instalar: 
o	Escolha a versão compatível com o seu sistema operacional e faça o download.
o	Execute o instalador e siga os passos para configurar o software, incluindo a criação de usuários e senha para acesso ao banco de dados.
o	Após a instalação, configure e teste o ambiente de trabalho conectando-se a um banco de dados.
3. Instalação do WampServer
•	Acesse o site oficial: https://www.wampserver.com.
•	Passos para instalar: 
o	Faça o download do instalador, garantindo que ele seja adequado ao seu sistema (32 ou 64 bits).
o	Antes de iniciar a instalação, baixe e instale as dependências Visual C++ Redistributable (vcredist), que são listadas no site oficial. Essas bibliotecas garantem o funcionamento correto do WampServer.
o	Execute o instalador do WampServer e configure o diretório de instalação.
o	Após a instalação, inicie o servidor local e verifique se os serviços do Apache e MySQL estão funcionando corretamente. O ícone na barra de tarefas deve estar verde para indicar que o servidor está ativo.
_______________________________________________________________________________________________________________________________________________________________________________________
**Explicação do Banco de Dados: controle-estoque**
### ⚙️ Configurações Iniciais

```sql
SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
START TRANSACTION;
SET time_zone = "+00:00";
```

- **SQL_MODE**: Permite inserir "0" em colunas com `AUTO_INCREMENT`, o que normalmente não é permitido.
- **START TRANSACTION**: Inicia uma transação, ou seja, um conjunto de comandos que só será aplicado com `COMMIT`.
- **time_zone**: Define o fuso horário como UTC (padronizado).

As linhas com `/*!40101` são comandos compatíveis com MySQL 4.1.1+ para configurar a codificação do banco.

---

### 📃 Criação do Banco de Dados

```sql
CREATE DATABASE IF NOT EXISTS `controle-estoque` ...
USE `controle-estoque`;
```

- Cria o banco de dados `controle-estoque`, se ainda não existir.
- Define que as próximas operações usarão esse banco.

---

### 📦 Tabela: `estoqueprodutos`

```sql
CREATE TABLE `estoqueprodutos` (
  NumeroLote INT PRIMARY KEY,
  NomeLote VARCHAR(100),
  Descricao VARCHAR(100),
  Preco FLOAT,
  Quantidade FLOAT,
  IdProduto BIGINT UNIQUE,
  DataEntrada DATETIME,
  DataSaida DATETIME
);
```

- Controla os **lotes de produtos**.
- `IdProduto` é `UNIQUE`, ou seja, cada produto pode estar ligado a apenas um lote.

---

### 🚚 Tabela: `fornecedor`

```sql
CREATE TABLE `fornecedor` (
  CNPJFornecedor VARCHAR(20) PRIMARY KEY,
  NomeFantasiaEmpresa VARCHAR(100),
  ...
);
```

- Armazena dados dos **fornecedores**.
- Inclui endereço, cidade, estado, telefone, email, etc.

Obs: o campo `CNPJFornecedor` é `VARCHAR`, mas é usado como `BIGINT` em outra tabela, o que pode causar erro.

---

### 🧱 Tabela: `materiaprima`

```sql
CREATE TABLE `materiaprima` (
  IdMateriaPrima BIGINT PRIMARY KEY,
  NomeMateriaPrima VARCHAR(100),
  ...
  CNPJFornecedor BIGINT UNIQUE
);
```

- Armazena **matérias-primas** usadas para fabricar produtos.
- `CNPJFornecedor` está com tipo `BIGINT`, diferente da tabela `fornecedor` (`VARCHAR`).
- `UNIQUE` em `CNPJFornecedor` limita a apenas uma matéria-prima por fornecedor.

---

### 📦 Tabela: `produto`

```sql
CREATE TABLE `produto` (
  IdProduto INT PRIMARY KEY,
  Nome VARCHAR(100),
  ...
  IdMateriaPrima BIGINT UNIQUE,
  DataEntrada TIMESTAMP,
  DataSaida TIMESTAMP
);
```

- Controla os **produtos fabricados**.
- `IdMateriaPrima` é `UNIQUE`, o que impede que a mesma matéria-prima seja usada por mais de um produto.

---

### 👤 Tabela: `users`

```sql
CREATE TABLE `users` (
  Login VARCHAR(100) PRIMARY KEY,
  Senha VARCHAR(100)
);
```

- Armazena logins e senhas dos **usuários do sistema**.
- Senhas armazenadas em texto puro (sem criptografia), o que não é seguro.

---

### ✅ Finalização da Transação

```sql
COMMIT;
```

- Finaliza a transação iniciada, salvando todas as alterações feitas.

---

### 🔄 Restaura Configurações

As configurações iniciais de conjunto de caracteres são restauradas ao final.

---

### 📊 Considerações Finais

- **Faltam chaves estrangeiras** para garantir integridade entre as tabelas.
- **Inconsistências de tipos** (ex: `CNPJFornecedor` com tipos diferentes).
- Uso de **UNIQUE** pode limitar o modelo de forma desnecessária.
- **Senhas em texto puro** precisam de criptografia para segurança.
____________________________________________________________________________________________
Descrição do modelo lógico* do banco de dados controle-estoque,
com base nas tabelas criadas. Um modelo lógico descreve *as entidades, atributos e os relacionamentos entre elas*, sem focar nos detalhes técnicos (tipo exato de dado, engine, etc).

---

## 🧠 *Modelo Lógico: Sistema de Controle de Estoque*

### **1. Entidade: Produto**
- *Atributos*:
  - IdProduto (PK)
  - Nome
  - Descricao
  - Preco
  - QuantidadeProduto
  - DataEntrada
  - DataSaida

- *Relacionamento*:
  - Usa *uma* Matéria-Prima → (1:1 ou N:1 dependendo da modelagem futura)

---

### **2. Entidade: MateriaPrima**
- *Atributos*:
  - IdMateriaPrima (PK)
  - NomeMateriaPrima
  - Descricao
  - Preco
  - Quantidade
  - DataEntrada

- *Relacionamento*:
  - É fornecida por *um* Fornecedor (1:1 no modelo atual, ideal seria N:1)

---

### **3. Entidade: Fornecedor**
- *Atributos*:
  - CNPJFornecedor (PK)
  - NomeFantasiaEmpresa
  - CEP
  - Endereco
  - Cidade
  - Estado
  - Telefone
  - Email
  - Bairro

- *Relacionamentos*:
  - Fornece muitas Matérias-Primas (idealmente 1:N)

---

### **4. Entidade: EstoqueProdutos**
- *Atributos*:
  - NumeroLote (PK)
  - NomeLote
  - Descricao
  - Preco
  - Quantidade
  - DataEntrada
  - DataSaida

- *Relacionamento*:
  - Contém *um* Produto (IdProduto como FK única → 1:1)

---

### **5. Entidade: Users**
- *Atributos*:
  - Login (PK)
  - Senha

- *Sem relacionamento com outras tabelas* (mas poderia haver vínculo com logs, permissões, etc).

---

## 📊 Resumo dos Relacionamentos

| Entidade Origem     | Relacionamento | Entidade Destino    | Cardinalidade (esperada) |
|---------------------|----------------|----------------------|---------------------------|
| Produto             | usa            | Matéria-Prima        | N : 1                     |
| Matéria-Prima       | fornecida por  | Fornecedor           | N : 1                     |
| EstoqueProdutos     | contém         | Produto              | 1 : 1                     |
_______________________________________________________________________________________________________________________________
