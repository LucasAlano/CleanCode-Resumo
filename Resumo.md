# 🧹🖥️ Introdução ao Código Limpo 

Este resumo aborda os principais pontos da apresentação sobre a introdução ao Clean Code, ministrada pelo Professor Ramon Venson na SATC em 2025.

## 💾 A Crise do Software 

Em 1968, a OTAN iniciou um projeto que formalizou o termo "Engenharia de Software" com o objetivo de discutir e implementar padrões de desenvolvimento.
Havia uma crescente demanda e complexidade de novos softwares, impulsionada pela expansão das redes de computadores.
A necessidade de criar novos métodos e ferramentas de desenvolvimento surgiu para suportar essa crescente demanda, visto que os métodos e a força de trabalho existentes não eram suficientes.

## 💥 Falhas de Software Históricas 

* **Caso Therac-25 (Década de 80):** Falhas no software das máquinas de radioterapia Therac levaram a 6 mortes entre 1985 e 1987. As causas incluíram:
    * Design ruim
    * Falta de testes adequados
    * Ausência de mensagens de erro informativas
    * Excesso de confiança
* **Caso Ariane 5 (1996):** A explosão do foguete Ariane 5, 39 segundos após o lançamento, causou um prejuízo de 370 milhões de dólares. A causa foi um **overflow**, resultante da tentativa de converter uma variável de 64 bits para uma de 16 bits em tempo de execução.
* Esses casos ilustram como falhas de software podem ter consequências graves e ressaltam a importância de práticas de desenvolvimento robustas.

## ✅ Como Evitar Falhas? 

Diversas práticas podem ajudar a prevenir falhas de software:

* Desenvolvimento Ágil
* Testes Automatizados
* Revisão de Código
* Arquitetura Limpa
* Programação Defensiva

## 🏆 Impactos do Código Limpo 

A adoção de práticas de Clean Code traz diversos benefícios:

* Redução de custos
* Maior produtividade
* Menos vulnerabilidades
* Mais facilidade na manutenção
* Escalabilidade de equipes

## ✨ O Que é Código Limpo? 

Código limpo é caracterizado por ser:

* Legível (Readability)
* Mantenível (Maintainability)
* Testável (Testability)
* Extensível (Extensibility)
* Elegante (Beauty)

## 🚧 Barreiras do Código Limpo 

Algumas barreiras podem dificultar a adoção de Clean Code:

* Ignorância
* Teimosia
* Arrogância
* Falta de Tempo

## 🖥️ Responsabilidade do Programador 

É responsabilidade de cada programador defender a qualidade do seu código e buscar a criação de código limpo.

## 📉 Débito Técnico 

* O Débito Técnico surge de implementações apressadas e sem planejamento, realizadas para atender a demandas imediatas.
* Com o tempo, o acúmulo de débito técnico pode levar a problemas de performance, segurança e escalabilidade.

## 📚 Práticas de Código Limpo 

* O livro "Clean Code" de Robert C. Martin popularizou o termo e oferece diversas diretrizes e princípios.
* É importante lembrar que o "Clean Code" é uma referência e não um dogma rígido.

## 🏷️ Nomenclaturas 

* Dar bons nomes a variáveis, funções, classes e outros elementos do código é crucial para a legibilidade.
* Phil Karlton (Netscape) famously disse: "Existem apenas duas coisas difíceis em ciências da computação: Invalidação de cache e dar nome as coisas."
* Bons nomes devem ser **intencionais**, **pronunciáveis**, **buscáveis**, e revelar a **intenção** da variável/função.
* Evitar desinformação, usar distinções significativas, usar nomes pronunciáveis e buscáveis, não usar codificações, usar nomes de classes e objetos como substantivos e verbos para métodos.

## 💬 Funções e Comentários 

* **Funções bem escritas valem mais do que mil comentários.** Um comentário mal escrito pode ser tão prejudicial quanto uma função mal escrita.
* Funções devem ser **pequenas**, fazer **uma única coisa** e fazê-la bem.
* Devem ter poucos argumentos (idealmente zero ou um).
* Evitar efeitos colaterais.
* Usar nomes descritivos.
* **Comentários devem ser usados com moderação**, principalmente para explicar o "porquê" e não o "o quê" do código.
* Bons comentários incluem informações legais, explicações de intenção, esclarecimentos, avisos e TODOs (com cautela).
* Maus comentários incluem murmúrios, redundância, informações enganosas, comentários obrigatórios, históricos e atribuições.

## 📏 Formatação e Estrutura 

* Grandes empresas de software frequentemente possuem padrões de formatação de código (exemplo: Google Java Style Guide).
* A formatação consistente facilita a leitura e compreensão do código.
* Manter a **coerência** na formatação dentro de um projeto é fundamental.

## 🐞 Tratamento de Erros 

* O primeiro bug de software registrado foi literalmente um inseto preso em um computador em 1947, documentado por Grace Hopper.
* O tratamento de erros é crucial para a robustez do software.
* Preferir o uso de **exceções** em vez de códigos de retorno para indicar erros.
* Fornecer mensagens de erro informativas.
* Realizar tratamento de erros de forma consistente.

## 🧪 Testes Unitários 

* Testes unitários testam uma **unidade de código isoladamente**.
* Idealmente, os testes são escritos **antes** do código (Test-Driven Development - TDD).
* Os testes devem ser executados **automaticamente** a cada atualização do código, garantindo que as alterações não introduzam novos bugs.

## 📚 Material de Apoio 

* Clean Code (Livro em Português e Inglês)
* As falhas numéricas que podem causar desastres (Artigo/Vídeo sobre falhas relacionadas a erros numéricos em software).


---
# ✨ Tópico 02 - Convenções e Nomenclaturas 

Este resumo detalha as convenções e a importância da escolha de bons nomes no Clean Code, com base na apresentação do Professor Ramon Venson na SATC em 2025.

## 🏷️ Nomenclaturas: A Base da Compreensão 

> "Existem apenas duas coisas difíceis em ciências da computação: Invalidação de cache e dar nome as coisas." - Phil Karlton, Netscape developer

A escolha de nomes adequados é fundamental para a clareza e manutenibilidade do código.

* **Impacto:** Estima-se que cerca de **70% do código-fonte do Eclipse** seja composto por nomes, evidenciando sua importância.
* **Para o computador:** `Sgu9Asd1M` e `blue` podem ser equivalentes.
* **Para o programador:** Nomes claros e significativos trazem inúmeras vantagens:
    * **Facilitam a compreensão:** Tornam o código mais intuitivo e rápido de entender.
    * **Reduzem a ambiguidade:** Eliminam dúvidas sobre o propósito de variáveis, funções e classes.
    * **Melhoram a comunicação:** Permitem que os desenvolvedores discutam o código de forma mais eficaz.
    * **Aumentam a manutenibilidade:** Código com bons nomes é mais fácil de modificar e corrigir.

## 🗂️ Categorias de Nomes 

A escolha do tipo de nome deve refletir a natureza do elemento de código:

* **Substantivos (com ou sem adjetivos):** Utilizados para **variáveis**, **constantes** e **classes**.
    * Exemplos: `usuario`, `analise_agenda`, `device_storage`, `user_profile`.
* **Verbos:** Utilizados para **funções** ou **métodos**, indicando a ação que realizam.
    * Exemplos: `save_user_profile`, `get_user_info`, `get_user_data`.

## ⚙️ Formas de Nomes para Funções 🔩

Caprile e Tonella identificaram seis categorias comuns de nomes para funções:

* **Ação Indireta:** Indicam que uma ação ocorrerá como resultado de um evento.
    * Exemplos: `error`, `on_error`, `on_error_callback`, `post_notification`.
* **Ação Direta:** Expressam uma ação clara e imediata.
    * Exemplos: `open`, `close`, `kill`, `start`, `stop`, `send`.
* **Ação sobre Objeto:** Descrevem uma ação realizada em um objeto específico.
    * Exemplos: `read_line`, `write_line`, `calculate_salary`, `update_status`.
* **Ação Dupla (Não Recomendado):** Funções que realizam duas ações distintas, tornando o código menos coeso.
    * Exemplos (a evitar): `search_and_replace_text`, `confirma_e_salva`, `validate_and_log`. É melhor dividir essas funções em duas separadas (`searchText` e `replaceText`, `confirm` e `save`, `validate` e `log`).
* **Checagem:** Funções que retornam um valor booleano indicando um estado. Geralmente prefixadas com `is`, `has`, `can`.
    * Exemplos: `is_valid`, `is_empty`, `is_valid_email`, `has_permission`, `can_edit`.
* **Transformação:** Funções que convertem um valor de um formato para outro. Geralmente prefixadas com `to`, `convert_to`.
    * Exemplos: `convert_to_hex`, `converte_para_binario`, `parse_json`, `format_date`.

* **Verbos Comuns:** No código fonte do Bash, os verbos mais utilizados são `get`, `set` e `make`. Sinônimos são usados para melhor clareza contextual (ex: `get_info`, `fetch_data`, `retrieve_value`).

## 🎯 Nomes com Significado: Clareza Acima de Tudo 

Utilize nomes que revelem o **conteúdo** ou o **propósito** do elemento de código. Um bom nome deve descrever **o que** o código faz, não **como** ele faz.

**Exemplo Ruim:**

```python
d = 50 # tempo decorrido em dias
print(d)
```
**Exemplo Bom:**

```Python

# en
days_since_modification = 50
print(days_since_modification)

# pt-br
dias_desde_modificacao = 50
print(dias_desde_modificacao)
```
## 🤥 Nomes Enganosos: Evite a Confusão 
Evite usar nomes que possam induzir o programador a erro. A consistência entre o nome e o comportamento é crucial.

**Exemplo Ruim:**

```python
accountList = Account()  # Sugere uma lista de contas, mas é uma única conta
```

**Exemplo Bom:**

```python
account = Account()  # Nome correto para uma única conta
```
Evite termos como "List" ou "Array" quando a variável armazena apenas um item.

## ↔️ Faça Distinções Significativas 
Crie distinções claras entre termos, especialmente quando as funções ou variáveis têm significados opostos ou complementares. Evite usar sinônimos fortes para funções diferentes.

**Exemplo Ruim:**

```python
def delete_user(user_id):
    # ...

def remove_user(user_id):
    # ...
```

**Exemplo Bom:**

```python
def delete_user(user_id):  # Remoção permanente
    # ...

def disable_user(user_id):  # Desabilita temporariamente
    # ...
```

---
# ✨ Tópico 03 - Convenções de Nomes 

Este tópico aborda as convenções de nomes utilizadas em programação para promover a consistência e a legibilidade do código.

## 🏷️ O Que São Naming Conventions?

Naming conventions são padrões que definem como os nomes de variáveis, funções, classes e outros elementos de código devem ser escritos. Elas facilitam a leitura e a manutenção do código, promovendo consistência entre diferentes desenvolvedores e projetos. Diferentes convenções são usadas dependendo do contexto, linguagem de programação e sistema operacional.

## 🗂️ Principais Tipos de Naming Conventions 

Existem diversas convenções de nomes comuns:

1.  **PascalCase:** Cada palavra começa com letra maiúscula, sem separadores (ex: `MyClass`, `UserController`).
2.  **camelCase:** A primeira palavra é em minúscula, e as subsequentes começam com maiúscula (ex: `myVariableName`, `getUserData`).
3.  **snake_case:** As palavras são todas em minúsculas e separadas por underscores (\_) (ex: `my_variable_name`, `get_user_data`).
4.  **kebab-case:** As palavras são em minúsculas e separadas por hifens (-) (ex: `my-variable-name`, `get-user-data`).
5.  **SCREAMING_SNAKE_CASE:** Igual ao snake\_case, mas todas as letras são maiúsculas (ex: `MY_CONSTANT_NAME`, `API_KEY`).
6.  **Hungarian Notation:** Usa prefixos para indicar o tipo ou propósito da variável (ex: `strName`, `intAge`).
7.  **Train-Case:** As palavras são separadas por hifens, com cada palavra começando em maiúscula (ex: `My-Variable-Name`).
8.  **Flatcase:** Todas as letras são minúsculas, sem espaços ou separadores (ex: `myvariablename`).

## ⚙️ Onde as Naming Conventions São Usadas? 

A tabela a seguir resume onde cada convenção é comumente utilizada:

| Convenção             | Linguagens/Sistemas        | Contexto de Uso                                        |
| :---------------------- | :------------------------- | :----------------------------------------------------- |
| PascalCase            | C#, Java, TypeScript       | Classes, Tipos, métodos em frameworks e APIs           |
| camelCase             | JavaScript, Swift, Java    | Variáveis e funções                                    |
| snake\_case           | Python, C, Ruby            | Funções, variáveis, nomes de arquivos                  |
| kebab-case            | CSS, HTML, URLs            | Classes CSS, nomes de arquivos web                     |
| SCREAMING\_SNAKE\_CASE | C, Python, Ruby            | Constantes                                             |
| Hungarian Notation    | C, Visual Basic            | Indicação de tipos em variáveis                        |
| Flatcase              | Sistemas compactos, arquivos | Nomes de arquivos e URLs curtos e compactados          |

## 📌 Outras Convenções Importantes 

* **Namespaces:** Estruturas hierárquicas para organizar código (ex: C#).
* **Nome de Arquivos e Pastas:** Regras específicas de sistemas operacionais (ex: underscores em Unix/Linux).
* **Web Naming Conventions:** kebab-case em URLs para legibilidade e SEO.

---
# ✨ Tópico 04 - Funções 

Este tópico aborda as diretrizes para escrever funções limpas e eficientes, conforme apresentado pelo Professor Ramon Venson.

## ⚙️ O Que São Funções? 

Funções são blocos de código que realizam tarefas específicas, podendo receber parâmetros, executar cálculos e retornar resultados.

## 🧼 Funções Limpas: Boas Práticas 

* **Pequenas:** Funções devem ser concisas, idealmente com no máximo 20 linhas.
* **Fazendo Uma Coisa:** Cada função deve ter uma única responsabilidade (Princípio da Responsabilidade Única - SRP).
    * **Exemplo:** Em vez de uma função que valida dados do cliente, verifica o status e processa o endereço, divida em `validateCustomerData`, `checkCustomerStatus` e `processCustomerAddress`.
* **Ordem de Leitura:** O código dentro das funções deve seguir uma ordem lógica e linear, facilitando a compreensão da história que o código conta.
* **Evitar Switches:** O uso excessivo de `switch` pode dificultar a manutenção. Considere o uso de tabelas de decisão ou polimorfismo.
    * **Exemplo:** Em vez de um `switch` para calcular o pagamento de diferentes tipos de funcionários, crie uma classe abstrata `Employee` com métodos abstratos como `calculatePay()`, implementados pelas subclasses específicas (`CommissionedEmployee`, `HourlyEmployee`, `SalariedEmployee`).
* **Nomes Significativos:** Nomes de funções devem ser verbos ou frases verbais que descrevam claramente a ação realizada (ex: `post_tweet`, `delete_user`, `calculate_total`).

## 📥 Parâmetros de Funções 

* **Poucos Parâmetros:** O ideal é zero parâmetros, seguido por um, dois ou três. Mais parâmetros tornam a função mais difícil de entender e testar.
* **Objetos como Parâmetros:** Se uma função precisa de muitos dados relacionados, considere passar um objeto contendo esses dados em vez de múltiplos parâmetros individuais.
    * **Exemplo:** Em vez de `sendEmail(String to, String from, String subject, String body, boolean isImportant)`, use `sendEmail(Email email)`.
* **Evitar Parâmetros Lógicos (Booleanos):** Um parâmetro booleano geralmente indica que a função faz mais de uma coisa. Considere dividir a função em duas.
    * **Exemplo:** Em vez de `render(Boolean isSilent)`, crie `render()` e `renderInSilentMode()`.
* **Evitar Efeitos Colaterais:** Funções devem evitar alterar o estado do programa fora de seu escopo de forma não óbvia.
    * **Exemplo:** Em vez de uma função `updatePhysics()` que também chama `RenderServer.update(this)`, separe as responsabilidades em `updatePhysics()` e `updateRender()`.
* **Evitar Parâmetros de Saída:** Parâmetros são geralmente para entrada. Usar parâmetros para saída (alterados dentro da função) dificulta a leitura. Prefira retornar valores.
    * **Exemplo:** Em vez de `add_to_list(List<String> list, String value)`, simplesmente chame `list.add(value)` no escopo onde a lista está definida.

## ⚖️ Separação Comando-Consulta 

Uma função deve ser um comando (realizar uma ação) ou uma consulta (retornar informações), mas não ambos.

* **Exemplo:** Em vez de `setUsername(String username)` que define o nome de usuário e retorna o novo nome (indicando sucesso), separe em `setUsername(String username)` (comando) e `getUsername()` (consulta).

## 🚫 Tratamento de Erros com Exceções 

* **Preferir Exceções a Códigos de Retorno:** Exceções tornam o tratamento de erros mais claro e separam a lógica de tratamento de erros do fluxo principal do código.
* **Extrair Blocos Try-Catch:** Para melhorar a legibilidade, o bloco `try-catch` pode ser extraído para uma função separada que lida apenas com o tratamento de erros.

## 🛠️ Evitar Repetição (DRY - Don't Repeat Yourself) 

Código duplicado dificulta a manutenção. Generalize funções semelhantes para evitar a repetição.


---
# ✨ Tópico 05 - Comentários 

Este tópico discute o uso de comentários no código, enfatizando que um código limpo geralmente requer menos comentários, conforme apresentado pelo Professor Ramon Venson.

## 📝 A Natureza dos Comentários 

Comentários são anotações no código usadas para comunicação entre programadores, documentando o que o código faz.

## 🚫 "Comentários são sempre fracassos." 

Um bom código deve ser autoexplicativo. A necessidade de um comentário muitas vezes indica que o código não está claro o suficiente. Comentários existem para explicar o que a linguagem de programação por si só não consegue expressar.

## 📉 Comentários Mascaram Código Ruim 

Quanto mais bem escrito o código, menor a necessidade de comentários. Refatore o código ruim em vez de apenas comentá-lo.

**Exemplo:**

Em vez de:
```python
<span style="color:red">
// Verifica se o funcionário é elegível para benefícios completos
if ((employee.flags & HOURLY_FLAG) && (employee.age < 65))
</span>
```

Use:
```python
<span style="color:green">
if (employee.isEligibleForFullBenefits())
</span>
```

## ✅ Bons Comentários (Usados com Moderação) 

* **Licenças de Software:** Informações legais sobre a licença, embora idealmente em um documento externo.
* **Explicação da Intenção:** Esclarecer o *porquê* de um código, não apenas o *quê*.
    * **Exemplo:** `// os espaços em branco são substituídos por %20 para evitar erros de URL`
* **Alerta de Consequências:** Avisar sobre os efeitos de certas alterações em partes críticas do código.
    * **Exemplo:**
  ```python
    <span style="color:red">
    // Executar esse teste apenas se tiver tempo disponível
    /*
    public void _testWithReallyBigFile() {
    // ...
    }
    */
    </span>
* **Comentários TODO:** Indicar tarefas futuras a serem implementadas (usar com cautela).
    * **Exemplo:** `
  ```python
  <span style="color:red">// TODO: Implementar lógica de cache</span>`
* **Documentação de API (Javadoc/Doxygen):** Para código que será distribuído como uma API.
    * **Exemplo:**
  ```java
  
    <span style="color:red">
    /**
     * Calcula o valor total com base no preço unitário e na quantidade.
     * @param unitPrice O preço de cada item.
     * @param quantity A quantidade de itens.
     * @return O valor total calculado.
     */
    public double calculateTotal(double unitPrice, int quantity) { ... }
    </span>

## ❌ Maus Comentários (A Serem Evitados) 

* **Murmúrios:** Comentários subjetivos ou que expressam a experiência pessoal do programador sem agregar valor.
    * **Exemplo:**
  ```java
  `<span style="color:red">// Nossa, essa parte foi difícil de entender!</span>`
* **Comentários Redundantes:** Comentários que simplesmente repetem o que o código já deixa claro. Código autoexplicativo é melhor.
    * **Exemplo:**
  ```java
    <span style="color:red">
    int count = 0; // Inicializa o contador com zero
    </span>
* **Comentários Enganosos:** Comentários que descrevem funcionalidades inexistentes ou incorretas. Devem ser corrigidos ou removidos imediatamente.
* **Comentários Imperativos:** Comentários que dão ordens ("// Garante que...") em vez de explicar.
    * **Exemplo:**
  ```java
  <span style="color:red">// Certifique-se de que a conexão com o banco de dados esteja aberta.</span>
* **Comentários Longos:** Blocos de comentários extensos geralmente indicam código complexo que poderia ser refatorado.
    * **Exemplo:**
  ```java
    <span style="color:red">
    /*
     * Esta seção do código lida com a autenticação do usuário.
     * Primeiro, verifica se as credenciais fornecidas são válidas consultando o banco de dados de usuários.
     * Em seguida, se as credenciais forem válidas, gera um token de sessão para o usuário.
     * Este token é armazenado em um cookie no navegador do usuário e é usado para autenticar solicitações subsequentes.
     * Caso as credenciais sejam inválidas, uma mensagem de erro é exibida ao usuário.
     */
    </span>
* **Comentários Ruidosos:** Comentários excessivos que obscurecem o código e dificultam a compreensão de lógicas simples.
    * **Exemplo:**
  ```java
    <span style="color:red">
    // INÍCIO DA FUNÇÃO
    public void processData() {
        // DECLARAÇÃO DE VARIÁVEL
        int value;
        // ATRIBUIÇÃO DE VALOR
        value = 10;
        // FIM DA FUNÇÃO
    }
    </span>
* **Marcadores de Posição:** Usar comentários para marcar seções longas de código (ex: `// ------- ATRIBUTOS ------`). Considere dividir o código em arquivos ou classes menores.
    * **Exemplo:**
  ```java
    <span style="color:red">
    public class Foo {
        // ------- ATRIBUTOS ------
        private String name;
        // ------- CONSTRUTOR ------
        public Foo(String name) {
            this.name = name;
        }
        // ------- GETTERS ------
        public String getName() {
            return name;
        }
        // ------- SETTERS ------
        public void setName(String name) {
            this.name = name;
        }
    }
    </span>
* **Comentários no Final da Linha:** Podem ser difíceis de ler e manter consistentes. Prefira comentários acima do código que descrevem.
    * **Exemplo:**
  ```java
  <span style="color:red">return sdf.format(date); // O padrão do SimpleDateFormat é "dd/MM/yyyy"</span>
* **Informações de Controle de Versão (Autoria, Data, etc.):** Essas informações são melhor gerenciadas por sistemas de controle de versão. Evite incluí-las como comentários no código.
    * **Exemplo:**
  ```java
    <span style="color:red">
    // Autor: John Doe
    // Data: 2023-07-28
    public class Foo { ... }
    </span>

## 💡 Substitua Comentários por Funções 

Se você precisa comentar um trecho de código para explicar o que ele faz, considere extrair esse trecho para uma função bem nomeada. Isso torna o código mais legível e autoexplicativo.

## 📍 Posição dos Comentários 

Um bom comentário geralmente está posicionado logo acima do código que ele descreve.

## 💾 Comentários vs. Controle de Versão 

Informações como autor, data de criação/atualização e linhas editadas são melhor rastreadas por sistemas de controle de versão. Evite incluí-las como comentários no código.

---
# ✨ Tópico 06 - Estrutura e Formatação 

Este tópico aborda a importância da estrutura e formatação do código para clareza e manutenibilidade, conforme apresentado pelo Professor Ramon Venson.

## 🎯 Objetivo da Formatação 

A formatação do código visa esclarecer a comunicação. Uma boa formatação persiste mesmo quando a funcionalidade do código muda.

## 📐 Formatação Vertical 

* **Arquivos Curtos:** Arquivos com menos linhas são mais fáceis de ler e compreender.
* **Metáfora do Jornal:** O código deve ser estruturado como um artigo de jornal, com os conceitos mais importantes no topo e detalhes progressivamente adicionados.
* **Espaçamento Vertical:** Linhas em branco separam conceitos diferentes, tornando a estrutura do código mais evidente. Funções e métodos geralmente são separados por uma ou mais linhas em branco.
    * **Exemplo:**
    ```java

    <span style="color:green">
    import db from 'db';

    const baseUrl = 'https://api.example.com';

    function getUser(id) {
        const user = db.get(id);
        return user;
    }

    function setUser(user) {
        db.set(user);
    }
    </span>
* **Continuidade Vertical:** Conceitos relacionados devem permanecer juntos. Espaços arbitrários entre linhas relacionadas dificultam a leitura.
    * **Exemplo:**
    ```java

    <span style="color:green">
    public project(axis: Vector): Projection {
        const scalars = [];
        const point = this.center;
        const dotProduct = point.dot(axis);
        scalars.push(dotProduct);
        scalars.push(dotProduct + this.radius);
        scalars.push(dotProduct - this.radius);
        return new Projection(Math.min.apply(Math, scalars), Math.max.apply(Math, scalars));
    }
    </span>
* **Distância Vertical:** A distância vertical entre a declaração e o uso de elementos (variáveis, funções) deve ser mínima.
* **Declaração de Variáveis:** Variáveis devem ser declaradas o mais próximo possível de sua primeira utilização, exceto variáveis de escopo amplo.
    * **Exemplo:**
    ```java

    <span style="color:green">
    function createMainElement(tag) {
        const element = document.createElement(tag);
        element.classList.add('new-class');
        const mainElement = document.querySelector('.main-element');
        mainElement.appendChild(element);
        return mainElement;
    }
    </span>
* **Declaração de Atributos:** Em orientação a objetos, atributos são geralmente declarados no início da classe, logo após a assinatura. A consistência é importante para saber onde encontrá-los.
    * **Exemplo:**
    ```java

    <span style="color:green">
    class User {
        nome: string;
        idade: number;
        altura: number;

        updateNome(nome: string) {
            this.nome = nome;
        }
        updateIdade(idade: number) {
            this.idade = idade;
        }
        updateAltura(altura: number) {
            this.altura = altura;
        }
    }
    </span>
* **Funções Dependentes:** Funções que chamam outras devem estar próximas umas das outras na ordem de chamada (top-down ou bottom-up).
    * **Exemplo:**
    ```java

    <span style="color:green">
    function makeRequest(url) {
        /* ... */
        const response = fetch(url);
        /* ... */
    }

    function fetch(url) {
        /* ... */
        resolveUrl(url);
        /* ... */
    }

    function resolveUrl(url) {
        /* ... */
    }
    </span>
* **Afinidade Conceitual:** Variáveis e funções relacionadas conceitualmente devem ser mantidas juntas. A ordenação alfabética também pode ser usada para facilitar a localização.
    * **Exemplo:**
    ```java

    <span style="color:green">
    const userController = new UserController(userService);
    const userService = new UserService(userRepository);
    const userRepository = new UserRepository();

    const mapaController = new MapController(mapaService);
    const mapaService = new MapService(mapaRepository);
    const mapaRepository = new MapRepository();

    const petController = new PetController(petService);
    const petService = new PetService(petRepository);
    const petRepository = new PetRepository();
    </span>
* **Ordenação Vertical:** Em código top-down, funções de alto nível vêm primeiro, seguidas pelas de nível inferior. O oposto se aplica ao código bottom-up.

## ↔️ Formatação Horizontal 

* **Linhas Curtas:** Geralmente, uma linha deve fazer apenas uma coisa. Evitar linhas excessivamente longas (recomenda-se entre 80 e 120 caracteres).
* **Espaçamento Horizontal:** Usar espaços para separar elementos não intimamente ligados e para melhorar a legibilidade de operadores. Não usar espaços para separar o nome da função dos parênteses.
    * **Exemplo:**
    ```java

    <span style="color:green">
    function soma(a, b) {
        return a + b;
    }
    soma(1, 2);
    </span>
* **Alinhamento Horizontal:** Alguns programadores alinham horizontalmente declarações ou atribuições. Embora possa parecer agradável, pode dificultar a manutenção se os nomes mudarem.
    * **Exemplo (opcional):**
    ```java

    <span style="color:green">
    class Pessoa {
        public    String nome;
        protected Integer idade;
        protected Double  altura;
        private   Double  peso;
    }
    </span>
* **Indentação:** A indentação visualiza a estrutura hierárquica do código (blocos de código dentro de condicionais, loops, funções, classes). A maioria dos editores de código automatiza isso.
    * **Exemplo:**
  ```java

    <span style="color:green">
    class Pessoa {
        nome: string;
        idade: number;
        altura: number;
        constructor(nome: string, idade: number, altura: number) {
            this.nome = nome;
            this.idade = idade;

            if (altura > 0) {
                this.altura = altura;
            } else {
                this.altura = 0;
            }
        }
    }
    </span>
* **Escopos Minúsculos:** Blocos de código pequenos (em lambdas, condicionais simples) podem ser mantidos em uma única linha, mas a clareza deve ser priorizada.
    * **Exemplo:**
  ```java

    <span style="color:green">
    lista.map(item => item.id);
    </span>

## 🤝 Regra de Equipes 

Equipes devem definir e seguir um padrão de formatação consistente para garantir que todo o código seja fácil de entender por todos os membros. Priorize a consistência em prol do sucesso da equipe, mesmo que signifique usar um estilo diferente do seu preferido.


---
# ✨ Tópico 07 - Linters 

Este tópico aborda a utilização de Linters para garantir a consistência e qualidade do código, conforme apresentado pelo Professor Ramon Venson.

## ✍️ Estilo e Documentação 

É crucial que todas as boas práticas e convenções de estilo a serem seguidas pela equipe de desenvolvimento sejam claramente documentadas.

## 📑 Style Guides 

Style guides são documentos que descrevem as convenções de estilo específicas que uma equipe deve seguir. Eles garantem que todos os desenvolvedores adotem os mesmos padrões de formatação, indentação, nomenclatura e outras diretrizes, evitando inconsistências e facilitando a manutenção do código.

**Exemplo de diretrizes em um Style Guide:**

* Espaço entre parâmetros: Sim
* Espaço entre o nome da função e parênteses: Não
* Espaço entre parênteses e o parâmetro: Não
* Indentação: 2 espaços
* Chave de abertura `{`: Na mesma linha, após um espaço
* Espaços ao redor de operadores: Sim (um espaço)
* Espaço após `for`/`if`/`while`: Sim
* Ponto e vírgula `;`: Obrigatório
* Espaço entre argumentos: Sim
* Linhas não muito longas
* Linha vazia entre blocos lógicos
* `else {`: Sem quebra de linha
* Espaços ao redor de uma chamada aninhada: Sim

## 🛠️ Linters: Automatizando a Qualidade 

Linters são ferramentas de análise estática de código que examinam o código-fonte em busca de problemas de formatação, erros comuns e inconsistências de estilo, com base em regras configuráveis. Eles podem ser personalizados para se adaptar aos style guides específicos de cada equipe.

## ⚙️ Tipos de Linters 

* **Linter de estilo:** Foca na análise da formatação do código, indentação e convenções de nomenclatura.
* **Linter de qualidade:** Avalia a qualidade do código, identificando potenciais problemas de desempenho, bugs e outras questões.

## 🔌 Integração dos Linters 

* **IDEs:** Linters podem ser integrados diretamente aos Ambientes de Desenvolvimento Integrado (IDEs), fornecendo feedback imediato aos desenvolvedores sobre problemas no código enquanto escrevem.
* **Pipelines de CI/CD:** Linters são frequentemente utilizados em pipelines de Integração Contínua e Entrega Contínua (CI/CD). Isso permite que problemas de estilo e qualidade sejam detectados automaticamente quando um novo código é enviado ao repositório, antes de ser integrado ao código principal.

## 🛠 populares 

* **JavaScript:** ESLint, Prettier
* **Python:** Flake8, Black
* **Ruby:** Rubocop
* **PHP:** PHPStan
* **Java:** SonarLint, Checkstyle
* **C e C++:** Clang-tidy

  ---
  # ✨ Tópico 08 - Estruturas de Dados 

Este tópico explora a importância da escolha e abstração de estruturas de dados para um código limpo, conforme apresentado pelo Professor Ramon Venson.

## ⚙️ Representação de Dados 

Dados podem ser representados de diversas formas, como structs, classes, arrays, dictionaries (maps), records, etc. A escolha da estrutura influencia como os dados são organizados e manipulados.

## 🛡️ Abstração de Dados 

Abstrair a representação interna dos dados permite flexibilidade e consistência na manipulação.

**Exemplo:**

A classe `Ponto` inicialmente expõe diretamente suas coordenadas `x` e `y`:
```java
<span style="color:red">
public class Ponto {
    public Double x;
    public Double y;
}
</span>
````
Ao invés disso, uma interface `Ponto` pode abstrair a representação, permitindo coordenadas cartesianas ou polares:

```java
<span style="color:green">
public interface Ponto {
    private Double getX();
    private Double getY();
    private Double getR();
    private Double getTheta();
    void setCartesiano(Double x, Double y);
    void setPolar(Double r, Double theta);
}
</span>
```

Essa abstração garante que as coordenadas possam ser lidas independentemente da representação interna, enquanto as alterações são feitas de forma consistente.

## ⚖️ Anti-simetria Dado/Objeto

Objetos podem ser vistos como manipuladores de outros objetos ou como objetos sendo manipulados (objetos de valor ou POJOs - Plain Old Java Objects). É importante distinguir esses papéis.

## 📜 A Lei de Demeter 

"Um módulo não deve enxergar o interior dos objetos que ele manipula." Um método só deve chamar métodos de:

1.  Sua própria classe.
2.  Um objeto passado como parâmetro.
3.  Um objeto criado dentro do próprio método.
4.  Um atributo do próprio objeto.

**Transgressão da Lei de Demeter (Exemplo):**
```java
<span style="color:red">
public class RegistroPonto {
    public void log(Funcionario funcionario) {
        String nomeSetor = funcionario.getSetor().getNome(); // Viola a Lei de Demeter
        Console.WriteLine("O setor " + nomeSetor + " fez um registro de ponto");
    }
}
</span>
```

## 🚂 Carrinhos de Trem 🚂

Cadeias longas de chamadas de métodos (`objeto.getA().getB().getC().fazerAlgo()`) são chamadas de "carrinhos de trem" e geralmente violam a Lei de Demeter, expondo a estrutura interna dos objetos.

**Exemplo:**
```java
<span style="color:red">
public class MusicPlayer{
    public void play(MusicFile music) {
        music.getArtist().getAlbum().getSong().play(); // Carrinho de trem
    }
}
</span>
```

## 🌊 Carrinhos de Trem vs. Interfaces Fluentes 

Interfaces fluentes (`new Order().setCustomer("John").setShippingAddress(...)`) podem parecer carrinhos de trem, mas não expõem a estrutura interna do objeto, sendo compatíveis com a Lei de Demeter.

## 🧬 Híbridos ibridos 🧬

Objetos devem ser claramente definidos como manipuladores de dados (com comportamento) ou como simples contêineres de dados (POJOs). Evite objetos híbridos com comportamento significativo e dados públicos.

## 📦 Objetos de Transferência de Dados (DTO) 

DTOs são classes simples com apenas variáveis públicas (ou acesso via getters/setters) e sem lógica de negócios. São usados para transferir dados entre camadas de uma aplicação.

**Exemplo (Java Record - forma concisa de DTO):**

```java
<span style="color:green">
public record Pessoa(String nome, String cpf);
</span>
```

Em vez de uma classe tradicional com getters e setters.

## 💾 Active Record 

Active Records são DTOs com métodos para persistência (como `save()` e `find()`). Regras de negócios não devem ser implementadas nesses objetos.

## 💡 Outras Dicas

* **Maps vs. Arrays:** Use arrays para coleções ordenadas ou processadas como um todo. Use maps para buscas rápidas por chave-valor.
* **Lists vs. Sets:** Use listas quando a ordem dos elementos importa e pode haver duplicados. Use sets quando a ordem não importa e não pode haver duplicados.
* **Evite Heranças Profundas:** Hierarquias de herança muito profundas são difíceis de entender e manter. Prefira composição.
    * **Exemplo (Usando Composição):**
      ```java
        <span style="color:green">
        public class Funcionario {
            private Pessoa pessoa;
            private Cargo cargo;
            private Setor setor;
        }
        </span>
* **KISS (Keep It Simple, Stupid):** Mantenha o código simples e fácil de entender. Evite complexidade desnecessária.
* **Polimorfismo vs. Condicionais:** Use polimorfismo (orientação a objetos) para escolher implementações diferentes em vez de longas cadeias de `switch/case` ou `if/else`.
* **Maps vs. Condicionais:** Em alguns casos, `switch/case` ou `if/else` podem ser substituídos por `Maps` e o padrão Strategy.
    * **Exemplo:**
  ```java
    <span style="color:red">
    # Condicionais
    if tipo == "Gerente":
        return Gerente()
    # Maps
    funcionarios = {
        "Gerente": Gerente()
    }
    </span>
* **Identidade vs. Igualdade:** Entenda a diferença entre comparar se dois objetos são a mesma instância na memória (identidade `==`) e se possuem os mesmos valores (`equals()` em Java, `==` e `__eq__` em Python). Objetos geralmente são comparados por identidade por padrão.
    * **Exemplo:**
  ```java

    <span style="color:red">
    nome1 = "Marta"
    nome2 = "Marta"
    nome1 == nome2 # True
    nome1 is nome2 # True (em muitos casos para strings literais)

    pessoa1 = Pessoa("Marta", "123456789")
    pessoa2 = Pessoa("Marta", "123456789")
    pessoa1 == pessoa2 # False (a menos que __eq__ esteja definido)
    pessoa1 is pessoa2 # False
    </span>
* **Passagem por Valor vs. Referência:** Tipos primitivos e Strings geralmente são passados por valor, enquanto objetos (incluindo coleções) são passados por referência. Alterações em objetos passados como parâmetro podem afetar o objeto original.
    * **Exemplo :**
  ```java

    <span style="color:red">
    def revisa_funcionarios(funcionarios):
        for funcionario in funcionarios:
            if funcionario['salario'] > 10000:
                funcionario['salario'] *= 1.1

    funcionarios = [
        {'nome': 'Ronaldinho', 'salario': 10000},
        {'nome': 'Marta', 'salario': 15000}
    ]
    revisa_funcionarios(funcionarios)
    # funcionarios agora foi modificado
    </span>

---
# ✨ Tópico 09 - Tratamento de Erros 

Este tópico explora as melhores práticas para tratamento de erros em código limpo, conforme apresentado pelo Professor Ramon Venson.

## 💥 O Que São Exceções? 

Exceções são um mecanismo robusto para tratamento de erros, permitindo a recuperação de situações inesperadas no programa.

## 🧱 Estrutura Básica de Tratamento de Exceções 

A maioria das linguagens utiliza uma estrutura `try-catch-finally` para lidar com exceções:

```java

<span style="color:green">
try {
    // Código que pode lançar uma exceção
}
catch (Exception e) {
    // Código para lidar com a exceção
}
finally {
    // Código que sempre será executado ao final, mesmo em caso de exceção
}
</span>
```

## 🚀 Lançamento de Exceções 

Exceções são lançadas (`throw` ou `raise`) quando uma condição excepcional ocorre, sinalizando um problema que precisa ser tratado.

## 💥 Let It Crash: Uma Filosofia Alternativa 

Linguagens como Elixir e Erlang adotam a filosofia "Let It Crash", onde programas devem falhar de forma rápida e explícita, facilitando a recuperação por um supervisor em vez de tentar tratar erros pontualmente.

## 📜 Sumário do Livro "Clean Code" sobre Tratamento de Erros 

* Use exceções em vez de códigos de erro.
* Crie primeiro o bloco `try-catch-finally`.
* Use exceções não verificadas (em linguagens como Java).
* Forneça contexto informativo nas mensagens de exceção.
* Defina o fluxo normal do programa separadamente do tratamento de exceções.
* Não retorne `null`.
* Não passe `null` como argumento.

## 🚫 Use Exceções em Vez de Códigos de Erro

Retornar códigos de erro dificulta a leitura e manutenção do código, obrigando o chamador a verificar o código de retorno após cada função. Exceções permitem um tratamento de erros mais claro e imediato.

**Exemplo (Em vez de código de erro):**

```java

<span style="color:red">
int dividir(int a, int b, int &resultado) {
    if (b == 0) {
        return -1; // Código de erro para divisão por zero
    }
    resultado = a / b;
    return 0; // Sucesso
}
int main() {
    int resultado;
    if (dividir(10, 0, resultado) == -1) {
        std::cerr << "Erro: divisão por zero!" << std::endl;
    } else {
        std::cout << "Resultado: " << resultado << std::endl;
    }
    return 0;
}
</span>
```

**Use exceções:**

```java

<span style="color:green">
int dividir(int a, int b) {
    if (b == 0) {
        throw std::runtime_error("Divisão por zero não permitida.");
    }
    return a / b;
}
int main() {
    try {
        int resultado = dividir(10, 0); // Retorna o resultado ao invés do erro
        std::cout << "Resultado: " << resultado << std::endl;
    } catch (const std::runtime_error &e) {
        std::cerr << "Erro: " << e.what() << std::endl;
    }
    return 0;
}
</span>
```

## 🏗️ Crie Primeiro o Bloco `try-catch-finally` 

Ao escrever código que pode lançar exceções, defina a estrutura de tratamento de erros (`try-catch-finally`) no início. Isso ajuda a esclarecer o escopo da operação e como os erros serão tratados, garantindo que o programa termine em um estado consistente (usando o bloco `finally`).

## ⚠️ Use Exceções Não Verificadas 

Em linguagens como Java, exceções verificadas (que devem ser explicitamente tratadas ou declaradas) podem levar a um acoplamento excessivo. Exceções não verificadas (como `NullPointerException`) oferecem mais flexibilidade. Se uma exceção verificada for lançada em um nível profundo da chamada de pilha, ela pode exigir declarações `throws` em várias camadas intermediárias.

**Exemplo (Java - Exceção Verificada):**

```java
<span style="color:red">
public class MissaoRebelde {
    public static void main(String[] args) {
        try {
            baseRebelde(); // A missão começa na base rebelde
        } catch (IOException e) {
            System.out.println(" Base Rebelde: Perdemos contato com Luke! " + e.getMessage());
        }
    }
    static void baseRebelde() throws IOException {
        System.out.println(" Base Rebelde: Enviando ordens para a Aliança...");
        aliancaRebelde();
    }
    static void aliancaRebelde() throws IOException {
        System.out.println(" Aliança Rebelde: Chamando Luke Skywalker para atacar!");
        lukeSkywalker();
    }
    static void lukeSkywalker() throws IOException {
        System.out.println(" Luke Skywalker: Mirando no reator da Estrela da Morte...");
        throw new IOException(" Erro crítico! O alvo foi perdido!"); // Lançando exceção
    }
}
</span>
```

## 💬 Forneça Contexto 

As mensagens de exceção devem ser informativas, fornecendo detalhes sobre o que estava acontecendo, onde ocorreu o erro e qual foi a causa.

## 🛣️ Defina o Fluxo Normal 

Separe a lógica de negócios do tratamento de exceções para manter o código principal claro. Use objetos de exceção para lidar com casos excepcionais.

**Exemplo (Em vez de verificar erros no fluxo principal):**

```java

<span style="color:red">
public void processOrder(Order order) {
    if (order == null) {
        System.out.println("Error: Order is null");
        return;
    }
    if (!order.isValid()) {
        System.out.println("Error: Invalid order");
        return;
    }
    try {
        orderProcessor.process(order);
    } catch (Exception e) {
        System.out.println("Processing failed: " + e.getMessage());
    }
}
</span>
```

**Use exceções para fluxos excepcionais:**

```java

<span style="color:green">
public void processOrder(Order order) {
    validateOrder(order);
    try {
        orderProcessor.process(order);
    } catch (ProcessingException e) {
        logError(e);
        throw new OrderProcessingException("O processamento da ordem de serviço falhou", e);
    }
}
private void validateOrder(Order order) {
    if (order == null || !order.isValid()) {
        throw new InvalidOrderException("A ordem de serviço é invalida");
    }
}
</span>
```


## 🚫 Não Retorne `null` 

Retornar `null` obriga os clientes a verificar explicitamente por valores nulos, levando a possíveis `NullPointerException`. Prefira lançar exceções ou usar o padrão Null Object ou Optional.

## 🚫 Não Passe `null` 

Passar `null` como argumento também é perigoso. Trate casos de parâmetros nulos lançando exceções ou usando `Optional`.

## 💡 Outras Dicas 

* **Padrão Objeto Nulo (Null Object Pattern):** Crie objetos substitutos que fornecem comportamento padrão em vez de `null`.
    * **Exemplo:** Em vez de retornar `null` para um cliente inexistente, retorne uma instância de `NullCliente` com valores padrão vazios.
* **Optional:** Use a classe `Optional` para representar valores que podem ou não estar presentes, forçando o cliente a verificar a presença do valor antes de acessá-lo.
* **Separe a Lógica de Negócios:** Mantenha o tratamento de erros fora dos métodos que implementam a lógica principal. Use controladores ou outras camadas para lidar com exceções.
* **Capture Apenas o Necessário:** Evite capturar `Exception` genérica. Capture exceções específicas para fornecer um tratamento mais significativo.
* **Use `finally` para Limpeza:** Garanta que recursos (arquivos, conexões) sejam fechados no bloco `finally` para evitar vazamentos, mesmo em caso de exceção.
* **Evite Falhas Silenciosas:** Não capture exceções sem tratá-las ou registr-las (logging). Isso pode mascarar erros importantes.
* **Logging:** Use logs estruturados em vez de apenas imprimir mensagens de erro no console para facilitar a análise e o monitoramento.
* **Não Use Exceções para Fluxo de Controle:** Exceções são para situações excepcionais, não para lógica de decisão regular (use `if-else` para isso). Exceções também são mais lentas que estruturas de controle.
* **Mensagens de Erro Significativas:** Forneça mensagens claras e informativas que ajudem a entender o problema, sem expor informações sensíveis ou detalhes de implementação internos.
* **Use Classes de Exceção Personalizadas:** Crie classes de exceção específicas do seu domínio para melhor categorização e compreensão dos erros.
* **Falhe Alto e Rápido:** Detecte e trate erros o mais cedo possível para evitar que se propaguem e causem problemas maiores.
* **Ferramentas de Monitoramento:** Utilize ferramentas como Sentry, Loggly, New Relic, Datadog e Rollbar para rastrear e analisar erros em produção.



