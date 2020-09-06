Select * from

(Select casa, sum(pontos) as total_casa from tabela group by casa) a

Left join

(select casa, aluno, sum(pontos) as total_aluno from tabela group by casa, aluno) b

On a.casa = b.casa
