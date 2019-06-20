O PROBLEMA DO CÁLCULO DE SALÁRIO
---
Suponha que uma empresa precise calcular o salário do funcionário e seus descontos. Para calcular esse desconto, a empresa leva em consideração o salário atual e o cargo do funcionário. Vamos representar funcionários e cargos da seguinte maneira:
```java
public enum Cargo {
    DESENVOLVEDOR,
    DBA,
    TESTADOR
}
public class Funcionario {
    
    private String nome;
    private double salario;
    private Cargo cargo;

    public Funcionario(String nome, double salario, Cargo cargo) 
    {
        this.nome = nome;
        this.salario = salario;
        this.cargo = cargo;
    }

    public String getNome() {
        return nome;
    }

    public double getSalario() {
        return salario;
    }

    public Cargo getCargo() {
        return cargo;
    }
}
  ```
Repare que um funcionário possui nome, salário e cargo. O cargo é representado por uma enumeração. Nesse momento, a enumeração contém apenas desenvolvedor, testador e DBA. Em uma situação real, essa enumeração seria maior ainda, mas com esses 3 já gera uma boa discussão.

As regras de negócio são as seguintes:

* Desenvolvedores possuem 20% de desconto caso seus salários sejam maiores do que R$ 3.000,00. Caso contrário, o desconto é de 10%.
* DBAs e testadores possuem desconto de 25% se seus salários forem maiores do que R$ 2.500,00. Em caso contrário, 15%.

Assim, utilizando TDD e passos de bêbê, evolua a classe **CalculadoraDeSalario** ao implementar o método **calculaSalario** a partir da classe de testes a seguir:
```java
public class CalculadoraDeSalarioTest {
    @Test
    public void deveCalcularSalarioParaDesenvolvedoresComSalarioAbaixoDoLimite()
    {
        //TODO
    }

}  
public class CalculadoraDeSalario {
    public double calculaSalario(Funcionario funcionario) 
    { 
        //TODO
    }
 
}
```
