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

Imagine que você tem uma lista com os seguintes elementos: [1, 2, 3, 4]. Agora, você quer remover o número 2 da lista. Se você executar a operação de remoção apenas uma vez, o resultado será: [1, 3, 4].

Se você executar a operação de remoção mais uma vez, o número 2 não estará mais na lista, então não haverá nada a ser removido e a lista final será a mesma: [1, 3, 4].

Se você executar a operação de remoção várias vezes seguidas, o resultado final ainda será o mesmo: [1, 3, 4]. Isso ocorre porque a operação de remoção é idempotente, ou seja, o resultado final da lista é o mesmo, independentemente do número de vezes que a operação é executada.



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

- D — Dependency Inversion principle

Módulo (ou Classe) de alto nível : Classe que executa uma ação com uma ferramenta.

Módulo de baixo nível (ou classe) : a ferramenta necessária para executar a ação

Abstração : Representa uma interface que conecta as duas Classes.

Detalhes : Como a ferramenta funciona

Módulos de alto nível não deve depender de módulos de baixo nível, e a abstração não deve depender dos detalhes, mas sim os detalhes à abstração.

### Designer Patterns

- Singleton

> O padrão singleton implica que deve haver apenas uma instância para uma classe. Em termos leigos, deve haver apenas um presidente por país de cada vez. Seguindo esse padrão, podemos evitar ter várias instâncias para uma classe específica.

- Factory 

>O padrão Factory simplesmente gera uma instância de objeto para um usuário sem expor nenhuma lógica de instanciação ao cliente. Ou seja, podemos atribuir varias funcionalidades sem a necessidade de especificamente ter uma ação direta. Em termos leigos: Não precisamos preprar um prato uma comida, podemos simplesmente compra-lá e ela virá pronta. Em programação basicamente fará desta forma, atribuíremos varias funcionalidades prontas e apenas atribuíremos isso que já está pronta. Assim facilitando a manutenção e extensão ou até implementação de um novo método dentro de um factory que já exista!

- Observer

> Um padrão Observer é uma forma de atualizar os dependentes quando há uma mudança de estado em outro objeto. geralmente contém Observere Observable. Observer subscreve Observablee onde há uma mudança, observável notifica os observadores. Resumindo: vamos supor que acessamos a rede social do twitter, dentro do twitter existe, seguidores, author e a propria publicação. Neste fluxo sempre um observará o outro, então quando houver uma nova publicação pode haver novos seguidores, que notificará o author e o autor notificará todo twitter, onde os seguidores visualizará. Ou seja, note que funciona basicamente em um loop, onde sempre um observará o outro!

- Fachada

> O padrão de fachada nos permite envolver funções ou módulos semelhantes dentro de uma única interface. Dessa forma, o cliente não precisa saber nada sobre como funciona internamente.Um bom exemplo disso seria inicializar seu computador. Você não precisa saber o que acontece dentro do computador quando o liga. Você só precisa apertar um botão. Dessa forma, o padrão de fachada nos ajuda a fazer lógica de alto nível sem a necessidade de implementar tudo pelo cliente.

-Abstract Factory 

>Permite produzir famílias de objetos relacionados sem especificar suas classes concretas.

-Build

>Permite construir objetos complexos passo a passo. O padrão permite produzir diferentes tipos e representações de um objeto usando o mesmo código de construção.

-Adapter

>Permite que objetos com interfaces incompatíveis colaborem.

-State

>Permite que um objeto altere seu comportamento quando seu estado interno muda. Parece que o objeto mudou de classe.


### Algums regras de clean code

1. Não utilizar má nomenclaturas em variáveis, classes, métodos ou nomes de arquivos

2. Evitar o uso de muitas dependências em instâncias

3. Se possível utilizar libs consolidadas e reduzir o número de classes, dessa forma dimunuímos a quantidade de código e consequentemente bugs.

4. Atentar-se para testes, os testes podem ajudar quebrar funcionalidades com o crescimento do sistema. Procure sempre uma boa cobertura de coverage!

5. Documente o que foi feito com muito detalhes, como se você estivesse escrevendo para alguém leigo na parte de tecnologia. 

6. Não deixa para refatorar quando o sistema já estiver muito grande. Faça isso o quanto antes, por que quanto mais atribuíções, mais díficil é separar responsabilidades.

7. Procure seguir padrões como SOLID, isso irá garantir que o seu sistema não vire uma bola de neve. 
        
        -Vantagens: 
                7.1. Classes únicas para cada responsabilidade
                7.2. Garantia de facilidade na manutenibilidade e extensão
                7.3. Não afetar diretamente o cliente quando houver modificação em alguma funcionalidade
                7.4. O cliente nunca deve ser forçado a utilizar algo que não tem necessidade
                7.5. Garantir que funcionalidades de alto nível não dependam de baixo nível

8. Usar códigos simples e fácil de ser interpretados para qualquer programador conseguir entender. 

9. Usar uma arquitetura clen, que vá além de um simples MVC. Exemplo: podemos adicionar camadas, de components, domains, presentation, e usar os designers patterns para garantir a padronização e funcionamento.




