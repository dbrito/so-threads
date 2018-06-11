# Documentação do Projeto sobre Threads

# Enunciado

Simule uma corrida de carros, em que cada carro é uma thread. Sorteie o tempo da volta aleatoriamente, variando entre 1 minuto e 2 minutos. A corrida terá 5 voltas. Mostre a classificação final por ordem de chegada.

## Conceito de Threads em java

Uma  `Thread`  no Java (a classe  `java.lang.Thread`) permite ao seu aplicativo Java rodar uma sequência de instruções em uma  _thread_  da máquina virtual, que na prática é executada por uma  _thread_  do sistema operacional hospedeiro ou  _kernel thread_  (lembrando que a máquina virtual do Java roda em cima de um sistema operacional hospedeiro).

Essas sequências de instruções são encapsuladas dentro de um método  `run()`  que é passado para o construtor da  `Thread`  (não o método diretamente, mas um objeto  `Runnable`, isto é, que implementa a interface  `Runnable`  e que portanto implementa o método  `run()`). Ou, alternativamente, uma vez que a própria classe  `Thread`  já implementa  `Runnable`, você pode optar por simplesmente implementar esse método no próprio objeto da classe  `Thread`.

Porém, somente dar um método  `run()`  à  `Thread`  não a faz rodar em paralelo a outras  _threads_. É necessário iniciá-la chamando o método  `Thread.start()`.
## Funcionamento do Projeto

O projeto possui duas classes principais **Corrida** e **Carro**. A classe Corrida fica responsável por instanciar os carros e dar a largada. A classe Carro que estende a classe `Thread ` quando instancia recebe o nome do piloto e o número de voltas que ele deve percorrer.

## Execução do projeto
Para executar o projeto basta rodar o comando `java -jar Corrida.jar` após isso o programa irá ser executado e irá mostrar um resultado parecido com o abaixo:
```
Corrida iniciada...
O corredor: Shumacker terminou a corrida. Tempo total(1:31)
O corredor: Senna terminou a corrida. Tempo total(1:49)
Corrida Finalizada```
