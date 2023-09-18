1 - Gerente com Dnumber 1 com ssn na tabela employer está como nulo, foi feito a substituição de "NULL" para o seu snn "888665555"
2 - Separado a coluna Address de employer por delimitador "-" para novas 4 colunas (Numer, Street, City, State)
3 - Foi mesclado a tabela employer com departament na propria tabela do employer usando o Super_snn, nesse processo foi selecionado apenas as colunas necessarias.
4 - Foi realizado a junção dos gerentes com os empregados utilizando SQl com seguin seguinte script:

SELECT 
    M.Fname AS Manager_Name,
    M.Ssn AS Manager_SSN,
    E.Ssn AS Employee_SSN
FROM 
    employee AS M
INNER JOIN 
    employee AS E
ON 
    M.Ssn = E.Super_ssn
5 - Colunas de Nome e Sobrenome foram mescladas
6 - Mesclado as tabelas departamento e localidade e depois mesclado departamento-local para criar uma coluna com valor único. No caso mesclar é a melhor opção visto que futuramente podem entrar novos departamentos e outras localidades e o atribuir não iria trazer a melhor solução para este caso.
7 - Para finalizar o visual foi criado em mente para verificar os projetos, horas trabalhas por empregado, projeto e gerente.