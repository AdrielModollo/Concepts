# Concepts


- Array.forEach “executa uma função fornecida uma vez por elemento da matriz.”

- Array.map “cria um novo array com os resultados de chamar uma função fornecida em cada elemento neste array.”


#### Find and Filter
O método find() é usado para encontrar todos os elementos descendentes do elemento selecionado. Ele encontra o elemento na árvore DOM percorrendo da raiz até a folha.

O método filter() é usado para filtrar todos os elementos e retorna o elemento que corresponde e os elementos que não correspondem são removidos.

A única diferença é que o método filter() pesquisa todos os elementos enquanto o método find() pesquisa apenas todos os elementos filhos.

````
Exemplo:
        1.Pedidos(Elemento Pai)
          2.Produto(Elemento Filho) 
          3.Produto(Elemento Filho)
````

#### idempotente

O termo “idempotente” em TI se refere a uma operação que não afeta o aplicativo em que é chamada, se for chamada mais de uma vez com os mesmos parâmetros de entrada. Outros tipos de operações alteram a estrutura de dados do aplicativo com cada iteração.

#### Diferença entre classe abstrata e interface abstrata

- Basicamente, a interface não permite a inserção de qualquer tipo de código, muito menos se ele for padrão. Já a classe abstrata pode oferecer uma codificação completa, o padrão ou apenas possuir a declaração de um esqueleto para ser sobrescrita posteriormente.

#### reduce
O método reduce()executa uma função redutora (fornecida por você) para cada elemento do array, resultando em um único valor de retorno


#### Redis

- Armazena os dados em memória cache, ou seja, caso a máquina seja reiniciada perderemos todos esses dados.

#### 4 Pilares POO

- Abstração: Conseguimos esconder os detalhes de algo, no caso, detalhes que não são necessários!

- Encapsulamento: Permite limitar e proteger o acesso ao nosso código. Exemplo: Um controle remoto, onde conseguimos acessar
sua interface(Ou seja seus botões), mas não conseguimos acessar seus circuitos por dentro e saber o que realmente está acontendo para realizar o funcionamento.

- Herança: Herda elementos de uma classe pai, desta forma podemos reproveitar funcionalidades que estão prontas em outras áreas do código.

- Polimorfismo: Conseguimos herdar e reutilizar partes do código prontas, mas diferente da herança, podemos atribuir comportamentos distintos.


#### Solid

- S — Single responsibility principle


Uma classe deve ter somente uma atribuíção. Exemplo: Temos um sistema que possuí apenas duas atribuições, salvar e atualizar, note que as duas funcionalidades são totalmente distintas, por tanto elas devem ser separadas em classes diferentes!


- O — Open closed principle

Aberto para extensão significa que devemos ser capazes de adicionar novos recursos ou componentes ao aplicativo sem quebrar o código existente.

Fechado para modificação significa que não devemos introduzir alterações importantes na funcionalidade existente , porque isso forçaria você a refatorar muito código existente 

Ou seja, deve ser aberto para extensão, mas devemos evitar introduzir alterações significativas em funcionalidades que ja existem e estão em operação.


- L — Liskov substitution principle

Uma subclasse deve substituir os métodos da classe pai de uma maneira que não interrompa a funcionalidade do ponto de vista do cliente.

- I — Interface segregation principle

Clientes não devem ser forçados a depender de métodos que não usam.

