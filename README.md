Relatório de cada processo executado no Desafio de Coleta e Processamento de Dados com Power BI.

Primeiramente foi criada uma instância na Azure para Mysql, em seguida foram construídas tabelas na Shell e preenchidas com os dados disponibilizados pela orientadora Julliana Mascarenhas no GuitHub. 

Fiz a conexão do banco de dados da Azure com o banco de dados Mysql Workbench, na sequência fiz uma integração do Power BI com o Mysql Azure e coloquei para transformar no Power Query.

Na planilha Departament excluí as colunas com as informações do banco value e table. Atualizei de número inteiro para texto a coluna Dnamber, renomeei a coluna Mgr_ssn para Super_ssn e reordenei.

Na planilha Dependent excluí as colunas com as informações do banco de dados value e mantive as demais informações que estavam bem estruturadas.

Na planilha Dept_locations excluí a coluna com as informações do banco de dados value, alterei a coluna Dnamber de números inteiros para texto, pois não precisa de cálculos e mantive as demais informações.

Na planilha Employee excluí as colunas com as informações do banco de dados com informações value e table. Na coluna Salary alterei o tipo para número decimal fixo e na coluna Dno para texto. Na coluna Super_ssn tinha um valor null e fiz o preenchimento para cima. Na coluna de endereço dividi coluna por delimitador separando número residência e alterando o tipo para texto, rua, bairro, cidade e substituí alguns valores. Renomeei a coluna Dno para Dnumber e Ssn para Essn.

Na planilha Project excluí as colunas com as informações do banco de dados value e table. Alterei o nome da coluna Dnum para Dnumber e alterei o tipo de todas as colunas para texto.

Na planilha Works_on excluí as colunas com as informações do banco de dados value. Renomeei a coluna Essn para ssn e Pno para Pnumber e alterei o tipo de inteiro para texto.

Foi feito uma mescla consulta como novas das tabelas Employee e Departament através do Dnumber, excluídas colunas desnecessárias, fiz reordenação das colunas e planilha renomeada para Funcionarios e Departamento.

Foi feito uma mescla consulta como novas das tabelas Employee e Departament através do Super_ssn, excluídas colunas desnecessárias. Planilha renomeada para Gerente e Funcionarios.

Foi feito uma mescla consulta como novas das tabelas Departament e Dept_locations através do Dnumber, excluídas colunas desnecessárias. Planilha renomeada para Departamento e Localização. Obs:  foi feito uma mescla e não uma atribuição, pois gera muitas linhas nulas pelo fato de não terem as mesmas estruturas, então, a melhor forma que encontrei além de mais prática foi fazendo a mescla, porque juntou todas as colunas e tive apenas que apagar as que não eram necessárias sem necessidade de mais transformações.

Foi feito uma mescla consulta como novas das tabelas Project e Work_on através do Pnumber, excluídas colunas desnecessárias. Planilha renomeada para Projeto e Hora, pois as tabelas constavam relacionamento, porém não estava fazendo a soma das horas.

Para finalizar criei um relatório com vários gráficos analisando alguns dados como por exemplo Quantidade de funcionários por departamento, salário por funcionários, quantidade de horas por projetos etc.
