#TODO

- Fazer as alterações necessárias para que seja possível editar os dados de usuário.

####Diferencial

- Adicionar mascaras e validações aos campos apresentados na aplicação.

#O que iremos analizar:

- Capacidade em identificar e solucionar os bugs existentes utilizando boas práticas de programação

#Dependências

Hibernate
Postgres

#Contribuidores
Antonio B Junior <antonio.barbosa@wssim.com.br>
Marcelo Fudo Rech <marcelo.rech@wssim.com.br>
Renan Viana Hoshi <renan.hoshi@wssim.com.br>

#Fase 2
##1º Exercício
TAGS: Fundamentos,Metamática,Algorítimo,Numeros,Jogos
O novo filme "Avengers" acaba de ser lançado! Há muitas pessoas na bilheteria do cinema em uma fila enorme. Cada um deles tem uma única nota de 100, 50 ou 25 reais. Um bilhete "Avengers" custa 25 reais.

Vasya está atualmente trabalhando como balconista. Ele quer vender um ingresso para cada pessoa nessa linha.

Pode Vasya vender um ingresso para cada pessoa e dar a mudança se ele inicialmente não tiver dinheiro e vender os ingressos estritamente na ordem que as pessoas seguem na fila?

Retorne SIM, se Vasya puder vender um ingresso para cada pessoa e dar o troco com as contas que ele tem em mãos naquele momento. Caso contrário, devolva NÃO.
Exemplos:

    Line.Tickets(new int[] {25, 25, 50}) // => YES
    Line.Tickets(new int[]{25, 100}) // => Não. Vasya não terá dinheiro suficiente para trocar 100 reais
    Line.Tickets(new int[] {25, 25, 50, 50, 100}) // => NO. Vasya não terá as notas certas para dar 75 reais de troco (você não pode fazer duas notas de 25 de uma 50)

Testes:

    import org.junit.Test;
    import static org.junit.Assert.assertEquals;
    import org.junit.runners.JUnit4;

    public class LineTests {
        @Test
        public void test1() {
          assertEquals("YES", Line.Tickets(new int[] {25, 25, 50}));
        }
      @Test
      public void test2() {
          assertEquals("NO", Line.Tickets(new int []{25, 100}));
        }
    }

Solução:

    public class Line {
      public static String Tickets(int[] peopleInLine)
      {
        //seu código aqui...
      }
    }

##2º Exercício
TAGS:Fundamentos, Otimização
Sua tarefa é construir um edifício que será uma pilha de n cubos. O cubo na parte inferior terá um volume de n^3, o cubo acima terá volume de (n-1)^3 e assim por diante até o topo, que terá um volume de 1^3.

Você recebe o volume total m do edifício. Sendo dado m, você pode encontrar o número n de cubos que você terá que construir?

O parâmetro da função findNb (find_nb, find-nb, findNb) será um inteiro m e você deve retornar o inteiro n tal como n^3 + (n-1)^3 + ... + 1^3 = m se n existir ou -1 se não houver n.
Exemplos:

    findNb(1071225) --> 45
    findNb(91716553919377) --> -1

    mov rdi, 1071225
    call find_nb            ; rax <-- 45

    mov rdi, 91716553919377
    call find_nb            ; rax <-- -1

Testes:

    import static org.junit.Assert.*;
    import org.junit.Test;

    public class ASumTest {

      @Test
      public void test1() {
        assertEquals(2022, ASum.findNb(4183059834009L));
      }
      @Test
      public void test2() {
        assertEquals(-1, ASum.findNb(24723578342962L));
      }
      @Test
      public void test3() {
        assertEquals(4824, ASum.findNb(135440716410000L));
      }
      @Test
      public void test4() {
        assertEquals(3568, ASum.findNb(40539911473216L));
      }

    }

Solução:

    public class ASum {

      public static long findNb(long m) {
        //seu código aqui
      }
    }

##3º Exercício
TAGS: Fundamentos,Metamática,Algorítimo,Numeros,Utilidades
Implemente um metodo que aceite 3 valores inteiros a, b, c. O medo deve retornar true se o triangulo puder ser construído com os lados de determinado comprimento e falso em qualquer outro caso.

(Neste caso, todos os triângulos devem ter uma superfície maior que 0 para serem aceitos).
Exemplos:

    import static org.junit.Assert.\*;
    import org.junit.Test;

    public class TriangleTesterTest {
        @Test
        public void publicTests() {
            assertEquals(true, TriangleTester.isTriangle(1,2,2));
            assertEquals(false, TriangleTester.isTriangle(7,2,2));
        }
    }

Solução:

    class TriangleTester{
      public static boolean isTriangle(int a, int b, int c){
        //seu código aqui
      }
    }
