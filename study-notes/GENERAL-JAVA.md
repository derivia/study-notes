<details>
<summary>📖 Sumário de Conteúdo</summary>

- [Algoritmos e Estruturas de Dados](#algoritmos-e-estruturas-de-dados)
- [Spring Framework](#spring-framework)
- [Umas coisas soltas](#parte-ainda-não-muito-bem-organizada)
</details>


## Algoritmos e Estruturas de Dados
> Baseado no livro Algorithms - 4th edition - Robert Sedgewick | Kevin Wayne

-  [Fundamentos](#fundamentos)
-  [Ordenação](#ordenação)
-  [Busca](#busca)

## Fundamentos 

### Big-O

- Notação
    - Utilizando como exemplo Busca Binária
    - Big O = Pior caso - O(log n)
    - Big Theta = Média - Θ(log n)
    - Big Omega = Melhor caso - Ω(1);

```Java
/*
Um pequeno exemplo de algoritmo.

Algoritmo de Euclides - Encontrar o maior divisor comum inteiro de dois números inteiros não-negativos.

Onde p e q são os dois números e r o valor restante entre o módulo de p e q.
*/

public static int gcd(int p, int q) {
    if (q == 0) {
        return p;
    }
    int r = p % q;
    return gcd(q, r);
}
```

## Ordenação

- [Bubblesort](#bubblesort)

### Bubblesort
- Péssimo, nunca implementar em nada.
```Java
public static void bubbleSort(int[] arr) {
    int n = arr.length;
    for (int i = 0; i < n - 1; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
}
```

## Busca

- [Busca Linear](#busca-linear)
- [Busca Binária](#busca-binária)

### Busca linear
    Iteração sequencial em um array/lista, até encontrar o elemento ou percorrer todos elementos.

```Java
public static int buscaLinear(int[] arr, int alvo) {
    for (int i = 0; i < arr.length; i++) {
        if (arr[i] == alvo) {
            return i;
        }
    }
    return -1;
}
```

### Busca Binária
    Divisão pela metade repetida de um array/lista **ordenada**.

```Java
    public static int binarySearch(int[] arr, int target) {
        int left = 0;
        int right = arr.length - 1;
        while (left <= right) {
            int mid = left + ((right - left) / 2);
            if (target < arr[mid]) {
                right = mid - 1;
            } else if (target > arr[mid]) {
                left = mid + 1;
            } else {
                return mid;
            }
        }
        return -1;
```

## Spring Framework

## Injeção de Dependência

- Uma forma de tornar um componente desacoplado (fazendo com que ele dependa de abstrações de métodos) de algo que ele requer, geralmente, por meio de uma interface, assim, por exemplo, uma função que utiliza como base um Set em Java poderia ter sua "classe concreta" trocada de HashSet para TreeSet, alterando a performance, entre outras coisas, sem alterar o funcionamento pois as implementações compartilham dos mesmos métodos, e, também, ao invés de em tempo de compilação, seja construída essa relação em tempo de execução.
- Facilita os testes unitários.

---

### Código que não utiliza injeção de dependência

```Java
public class Motor {
    public void ligar() {
        System.out.println("Motor ligado.");
    }

    public void desligar() {
        System.out.println("Motor desligado.");
    }
}

public class Carro {
    private Motor motor;

    public Carro() {
        motor = new Motor(); // Aqui a dependência é criada internamente
    }

    public void dirigir() {
        motor.ligar();
        System.out.println("Carro em movimento.");
    }

    public void parar() {
        motor.desligar();
        System.out.println("Carro parado.");
    }
}
```

### Código que utiliza injeção de dependência

```Java
// Interface que define o "contrato" de um motor
public interface Motor {
    void ligar();
    void desligar();
}

// Implementação concreta da interface Motor
public class MotorPadrao implements Motor {
    @Override
    public void ligar() {
        System.out.println("Motor ligado.");
    }

    @Override
    public void desligar() {
        System.out.println("Motor desligado.");
    }
}

// Classe Carro agora depende da interface Motor
public class Carro {
    private Motor motor;

    public Carro(Motor motor) {
        this.motor = motor; // Injeção da dependência via construtor
    }

    public void dirigir() {
        motor.ligar();
        System.out.println("Carro em movimento.");
    }

    public void parar() {
        motor.desligar();
        System.out.println("Carro parado.");
    }
}
```

### Exemplo em spring

```Java
@Service
public class StudentService {
    private final StudentRepository studentRepository;

    @Autowired
    public StudentService(StudentRepository studentRepository) {
        this.studentRepository = studentRepository;
    }

    // Código que utiliza métodos de StudentRepository
}

@Repository
public class StudentRepository extends JpaRepository<StudentEntity, Integer> {
    // StudentRepository extends JpaRepository, herdando seus métodos e JpaRepository recebe como "parâmetro" o objeto a ser trabalhado e o tipo da chave primária
    // Código que interage com o banco de dados
}
```
---

## Inversão de Controle

- O Spring se torna responsável pelo gerenciamento de diversos componentes da aplicação, as Beans, que têm seu ciclo de vida e conexões baseados na interpretação do Spring das annotations nas classes/métodos.

## Arquitetura Limpa

- Dividido em camadas a fim de atingir proteção às regras de negócio.

- Entidades: A camada mais interior, representa as classes mais simples que refletem os conceitos do negócio.

- Casos de uso: Responsável pela implementação das regras de negócio.

- Interface: Atua como uma ponte para os casos de uso (as regras de negócio) poderem utilizarem as entidades.

- Framework e Drivers: Onde ficam as coisas de terceiros, como Spring Web, o Spring JPA, Driver MySQL/Postgres.

## Alguns pontos soltos aqui pra que eu possa me alinhar mais tarde.

- Spring é dividido em módulos para que o desenvolvedor seja capaz de utilizar apenas aquilo que lhe é necessário. 
    
- Spring e Spring Boot são coisas diferentes, o Spring Boot surge com o intuito de diminuir a verbosidade do código Spring e facilitar o gerenciamento de dependências.
    
- Pom.xml é semelhante ao package.json de NodeJS.
    
- JPA: Um padrão estabelecido como uma interface para que bibliotecas implementem ORM.
    
- ORM: Tipo de biblioteca para relacionar objetos da linguagem à tabelas SQL.
    
- JDBC: A biblioteca do Java para comunicação com banco de dados, utiliza queries SQL "puras". O JPA "programifica" essa biblioteca, ofuscando o SQL.
    
- JWT: Uma tecnologia de segurança que permite o acesso aos dados somente quando o token JWT é enviado junto às requisições feitas pelo usuário. Pode ser colocada tanto no localstorage/sessionstorage, mas pelo visto é mais comum e recomendado ser colocados em cookies. Apesar de que ambas abordagens têm seus respectivos problemas de segurança.

## **TODO:** Sistemas Operacionais

## Como funciona um sistema operacional no geral

## Gerenciamento de Memória

## Armazenamento

## Coordenação de processos

## Comunicação entre processos

## Threads, concorrência e paralelismo

## Input/Output


## **TODO:** O que é, como funciona, como configurar e quando usar:

## Firewall

## Reverse Proxy

## Forward Proxy

## Load Balancer

## Docker

## VPN

## CI/CD

## Parte ainda não-muito-bem-organizada

## Testes

- Test Driven Development
    - Um conceito (caminho) a se seguir desde o começo do desenvolvimento da aplicação, como o próprio nome diz, a aplicação é desenvolvida tendo como base os testes.

- Tipos de testes
    - Unit Testing: Realizados em partes pequenas como funções/métodos, geralmente utilizando objetos mock como parâmetro.

    - Integration Testing: Realizados em conexões entre diferentes partes da aplicação.

---

## APIs

- REST
    - Dialoga por meio de JSON, XML, HTML, etc.
    - Geralmente utilizado em aplicações modernas e APIs públicas.  
    - Dependente do protocolo de transporte HTTP.
- SOAP
    - Dialoga por meio de XML.
    - Geralmente utilizado em aplicações legado e APIs privadas.
    - Independente de protocolo de transporte.

---

## Bancos de dados

- Diferentes DBMSs
    - DBMS
        - Principal: Não é estritamente relacional.
        - Exemplos: Cassandra e MongoDB.
    
    - RDBMS
        - Principal: É estritamente relacional.
        - Exemplos: MySQL e SQLite.
    
    - ORDBMS
        - Principal: Orientação a objetos.
        - Exemplo: Postgres com herança e métodos.

- ORM (Object Relational Mapping)
    - Conceito de relacionar 1 para 1 um objeto da linguagem com a tabela SQL, tornando possível utilizar de um paradigma orientado a objetos para interagir com um banco de dados.

- ACID (Atomicity, Consistency, Isolation and Durability) 
    - Uma série de padrões transacionais implementados pelas DBMS a fim de manter a integridade.

- Transactions 
    - Uma sequência de diversas operações realizadas em um DB específico. O objetivo é seguir o A de ACID (Atomicity), fazer com que quando essas operações acontecerem, acontecerem apenas por completo. 

- N+1 
    - Um problema em que ocorrem diversas queries para buscar dados que poderiam ter sido buscados em menos queries.

- Normalização
    - Reduzir a redundância por meio de dividir as tabelas e relacionar elas, do ponto de vista de design pode parecer ótimo, mas pelo que entendo, a performance pode ser afetada.
    (grande aumento do número de joins)

### Tipos de NoSQL

- Document (MongoDB)
    - Armazena os dados em documentos.
    - Tipicamente utiliza JSON.
    - Pode parecer mais rápida, mas não necessariamente é.
    - Mais próximo do comum ao programador, por possuir similaridades a objetos de linguagens de programação.
    - Pros
        - Flexibilidade.
        - Trabalha melhor com estruturas de dados complexas.
- Realtime (Firebase)
    - Também utiliza JSON.
    - Não utiliza HTTP.
    - Utilizada para coisas em tempo real.
    - Pros
        - Baixa latência.
        - Sincronização em tempo real.
        - Ótima para trabalho colaborativo.
- Key-value (Redis)
    - Segue o modelo chave-valor. Onde uma chave possui um valor relacionado.
    - Dados são associados a uma única chave.
    - Flexibilidade no schema dos objetos trabalhados.
    - Geralmente utilizado como cache, por ser em memória.
    - Pros
        - Modelo simples.
        - Arquitetura escalável.
---

## Padrões de arquitetura

- Monolítico
    - Uma única aplicação é responsável por tudo.
    - Pros 
        - Fácil de manter.
    - Cons 
        - Pode se tornar muito lento muito rapidamente.
        - O fato de tudo estar junto pode levar a vários erros em uma simples mudança.
- Microserviços
    - Aplicações distribuídas comunicam entre si o que é necessário, definindo  saídas e entradas.
    - Pros
        - Escalação mais granular, é mais fácil escalar o que for necessário, devido à independência dos serviços.
    - Cons
        - Difícil de manter, pode se tornar muito complexo muito rapidamente.
- Serverless
    - O não gerenciamento de servidores (claro, ainda são servidores, mas há o servidor é abstraído 
    [já que programador adora essa palavra] do desenvolvimento da aplicação.)
    - Pros
        - Facilidade devido à abstração.
    - Cons
        - Menor personalização comparado à outras arquiteturas.
---

## **TODO:** GoF Patterns

- **Creational Design Patterns**
    - Abstract Factory
    - Builder
    - Factory Method
    - Prototype
    - Singleton

- **Structural Design Patterns**
    - Adapter
    - Bridge
    - Composite
    - Decorator
    - Facade
    - Flyweight
    - Proxy

- **Behavior Design Patterns**
    - Chain of Responsibility
    - Command
    - Interpreter
    - Iterator
    - Mediator
    - Memento
    - Observer
    - State
    - Strategy
    - Template Method
    - Visitor

## Umas coisas soltas

- HATEOAS
    - Um princípio de APIs RESTful para tornar autoexplicativo o uso da API, ao fornecer links para operações relacionadas.
    - Facilita com que o consumidor da API possa desfrutar das operações, geralmente um desenvolvedor, pois o cliente comum não utiliza o JSON da API "diretamente", apenas vê a formatação como o desenvolvedor front-end forneceu.

- Caching
    - Caching é uma forma de tornar mais rápida a resposta por meio de um maior uso de armazenamento.
    - Pode ser feito de várias formas, geralmente dividido entre server-side e client-side.
    - No caso de client-side, o cache é o armazenamento de recursos estáticos que tendem a mudar pouco e que serão muito acessados, fazendo com que o usuário acessando o mesmo, por exemplo, site, precise demandar menos recursos do servidor web pois o navegador checa se há o recurso armazenado no cache.
    - No caso de server-side, geralmente uma tecnologia de banco de dados é utilizada para acelerar as queries feitas em um banco de dados pai.
    - Também é como uma parte do DNS funciona, sites que foram abertos recentemente ficam armazenados em cache, para que não seja preciso consultar.

- CORS (Cross-origin Resource Sharing)
    - Um mecanismo de segurança, ajuda a prevenir ataques de origem cruzada (cross-origin), um servidor define as regras que determinam quais origens externas têm acesso aos recursos de um domínio.
    - Por isso não é possível executar as funções de um arquivo JS que dão fetch em uma API externa, que está sendo importado pelo arquivo HTML aberto no navegador, o CORS não está configurado.

- Model View Controller
    - Model
        - A lógica do negócio, gerenciamento das operações e regras.
    - Controller
        - A interface entre o visual e o modelo.
    - View
        - O visual da aplicação.

- SSL/TLS
    - Secure Socket Layer (Antigo)
    - Transport Layer Security (Novo)
    - Ambos baseados em certificados para tentar garantir um contrato de confiança entre cliente-servidor.

- RabbitMQ
    - Um serviço de mensageria em fila (um message broker ou queue manager).
    - Uma interface entre diferentes partes de uma aplicação ou diferentes aplicações, em fila.
    - Imagina que daqui alguns dias irá lançar um novo filme da marvel, vários usuários entram no site hipotético: filmes://ingressos.com.br e vão atrás de reservar seu ingresso para assistir o filme, porém, o sistema não utiliza uma fila para aguentar a alta demanda e falhas acontecem.
    - Uma fila deve ser implementada porque garante que **mesmo de forma lenta** a aplicação continue respondendo.

- Nginx
- Apache

- RPC

~ [De volta ao topo](#índice)
