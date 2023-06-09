# Exercício em grupo

- Neste exercício o aluno irá implementar um conjunto de menus interativos, ao qual mostra conteúdo semelhante à estrutura existente no Moodle da Universidade Lusófona.

## Conteúdo esperado:

![](./img/menu_moodle.png)

## Regras:

- O aluno deverá implementar o código em C.
- Quando chegamos no fim da árvore de opções, o programa deve imprimir `Opcao X escolhido`, onde `X` deve ser substituído pelo número da opção `e volta a exibir o menu`.
- Quando alguma opção inválida for digitada, imprimir `Opcao Invalida` e voltar a exibir o menu.
- O menu de calendário deve imprimir o calendário conforme o diagrama, onde houver evento exibir este no ecrã e voltar a imprimir o menu.
- A opção `Sair` retorna ao nível anterior na árvore.


## Exemplo de execução:

```bash
1 - Disciplinas
2 - Calendario 
0 - Sair 
>1
1 - Recursos Gerais
2 - LP1
3 - AED
4 - Matematica II
5 - Algebra Linear
6 - Arq. Computadores
7 - Comp Compormentais 
0 - Sair 
>3
1 - Anuncios
2 - Aulas Teoricas
3 - Aulas Praticas
4 - Notas Exames 
0 - Sair 
>3
Opcao 3 escolhido 
1 - Anuncios
2 - Aulas Teoricas
3 - Aulas Praticas
4 - Notas Exames 
0 - Sair 
>0
1 - Recursos Gerais
2 - LP1
3 - AED
4 - Matematica II
5 - Algebra Linear
6 - Arq. Computadores
7 - Comp Compormentais 
0 - Sair 
>0
1 - Disciplinas
2 - Calendario 
0 - Sair 
>2
1 - Fevereiro 
2 - Marco 
3 - Abril 
4 - Maio
5 - Junho
6 - Julho  
0 - Sair 
>6
1-15 Avaliacoes Recurso  
0 - Sair 
1 - Fevereiro 
2 - Marco 
3 - Abril 
4 - Maio
5 - Junho
6 - Julho  
0 - Sair 
>4
Opcao 4 escolhido 
1 - Fevereiro 
2 - Marco 
3 - Abril 
4 - Maio
5 - Junho
6 - Julho  
0 - Sair 
>5
10-17 Pausa
17-31 Avaliacoes Finais Freq  
0 - Sair 
1 - Fevereiro 
2 - Marco 
3 - Abril 
4 - Maio
5 - Junho
6 - Julho  
0 - Sair 
>0
1 - Disciplinas
2 - Calendario 
0 - Sair 
>0
``` 

Nota: No exemplo acima é usado o simbolo '>' para indicar quando utilizador insere dados, é meramente indicativo e este simbolo nao deve ser imprimido antes da inserção de dados.

## Dicas:

- O aluno pode usar funções para organizar, simplificar e reutilizar o código.

## Testes adicionais do pandora

Os dois ultimos testes pedem as seguinte alterações ao programa.

- Quando se lista o menu contendo os meses do calendário, apesar de não escrito se o aluno usar a opção 9 tambem ira sair do menu tal como usasse a opção 0.

- Quando aluno seleciona a opcao ' 4 - Notas Exames', o programa de seguida apresenta o menu da pagina inicial. O menu funciona de modo recursivo, ver exemplo em baixo.

```bash
1 - Disciplinas
2 - Calendario 
0 - Sair 
>1
1 - Recursos Gerais
2 - LP1
3 - AED
4 - Matematica II
5 - Algebra Linear
6 - Arq. Computadores
7 - Comp Compormentais 
0 - Sair 
>1
1 - Anuncios
2 - Aulas Teoricas
3 - Aulas Praticas
4 - Notas Exames 
0 - Sair 
>4
1 - Disciplinas
2 - Calendario 
0 - Sair 
>0
1 - Anuncios
2 - Aulas Teoricas
3 - Aulas Praticas
4 - Notas Exames 
0 - Sair 
>0
1 - Recursos Gerais
2 - LP1
3 - AED
4 - Matematica II
5 - Algebra Linear
6 - Arq. Computadores
7 - Comp Compormentais 
0 - Sair 
>0
1 - Disciplinas
2 - Calendario 
0 - Sair 
>0
``` 