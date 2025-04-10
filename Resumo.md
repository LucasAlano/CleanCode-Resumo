#   Resumo Completo de Clean Code 🚀

##   Tópico 01: Introdução ao Código Limpo 🧹

* **A Crise do Software:** Em 1968, a OTAN criou a Engenharia de Software para padronizar o desenvolvimento. 🤯 [cite: 24]
* **Aumento da Demanda:** A explosão das redes aumentou a necessidade de softwares, mas os métodos não acompanharam. 📈 [cite: 25, 26]
* **Caso Therac-25:** Falhas no código causaram acidentes graves nos anos 80. ☢️ [cite: 27]
* **Custo do Caos:** Código ruim atrasa projetos e aumenta custos. 💸
* **A Atitude Limpa:** Ser dev é ser responsável por escrever código limpo. 🧑‍💻
* **O que é Código Limpo?:**
    * Elegante e eficiente. ✨
    * Focado em fazer bem uma coisa. 🎯
    * Simples e direto. 🛤️
    * Fácil de ler e entender. 📖
    * Testável. ✅
    * Sem duplicação. 👯
* **Padrões:** Empresas como Google e Microsoft têm guias de estilo. 🏢
* **Legado:** Código limpo é um presente para o futuro. 🎁
* **Tratamento de Erros:** Inspirado por um inseto real! 🐛
* **Testes Unitários:** Testam pequenas partes do código isoladamente. 🧪

##   Tópico 02: Convenções e Nomenclaturas 🏷️

* **A Arte de Nomear:** Nomear é um dos desafios da programação. 🤯 [cite: 122]
* **Importância dos Nomes:** 70% do código do Eclipse são nomes! 😱 Nomes claros são cruciais. 🤓 [cite: 123]
* **Categorias de Nomes:**
    * **Variáveis, Constantes e Classes:** Substantivos (e adjetivos). Ex: `usuario`, `analise_agenda`. 🏷️ [cite: 126, 127]
    * **Funções e Métodos:** Verbos. Ex: `salvar_perfil`, `obter_info`. 🚀 [cite: 127]
* **Formas de Nomear Funções:**
    * Ação Indireta: `on_error_callback` ↩️ [cite: 129]
    * Ação Direta: `open`, `close`, `kill` 🚪 [cite: 130]
    * Ação sobre Objeto: `read_line`, `write_line` ✍️ [cite: 130]
    * **EVITE Ação Dupla:** `search_and_replace_text` (confuso!) 😵 [cite: 130]
    * Checagem: `is_valid`, `is_empty` ✅ [cite: 130]
    * Transformação: `convert_to_hex` ➡️ [cite: 130]
* **Verbos Comuns:** `get`, `set` e `make` são frequentes. 🥇 [cite: 131]
* **Nomes Significativos:**
    * Devem dizer o que FAZEM, não COMO fazem. 🎯 [cite: 133, 134]
    * Ex: `dias_desde_modificacao` é melhor que `d`. 🗓️ [cite: 137]
* **Evite Desinformação:**
    * Não use palavras com múltiplos significados. 😕
    * Cuidado com abreviações (ex: `acc` para `account`). ✂️
    * Não use nomes parecidos (ex: `xyz` e `xyzArray`). 👂
* **Faça Distinções Significativas:**
    * Use nomes diferentes para coisas diferentes. 💡
    * Não adicione números ou ruído (ex: `info` vs. `info1`). 🔢
* **Use Nomes Pronunciáveis:** Facilita a comunicação. 🗣️
* **Nomes de Classes:** Substantivos ou frases substantivas. 🏛️
* **Nomes de Métodos:** Verbos ou frases verbais. ⛹️‍♀️ `get` para acessar, `set` para alterar, `is` para booleanos.
* **Seja Esperto, Não Fofo:** `kill` é melhor que `delete`. 💥 Evite gírias. 🤡
* **Use Nomes de Domínio:** Use termos da área do problema. 🏥
* **Adicione Contexto Significativo:** `endereco_estado` em vez de `estado`. 🏠
* **Não Adicione Contexto Desnecessário:** Se a classe é `GerenciadorDeEstudantes`, não precisa de `GE_` em tudo. 🙄

##   Tópico 03: Convenções de Nomes ✍️

* **O que são Naming Conventions?:** Padrões para escrever nomes no código. [cite: 253, 254, 255]
* **Por que usar?:** Facilitam a leitura e manutenção. 🤝 [cite: 254]
* **Tipos de Naming Conventions:**
    1.  PascalCase: `NomeCompleto`
    2.  camelCase: `nomeCompleto`
    3.  snake\_case: `nome_completo` 🐍
    4.  kebab-case: `nome-completo` 🥙
    5.  SCREAMING\_SNAKE\_CASE: `NOME_COMPLETO` 📣
    6.  Hungarian Notation: `strNome`, `intIdade` (EVITAR!) ❌
    7.  Train-Case: `Nome-Completo`
    8.  Flatcase: `nomecompleto` 🗄️
* **Tabela de Convenções:**
    * `PascalCase`: C#, Java (Classes, Tipos)
    * `camelCase`: JavaScript, Swift (Variáveis, Funções)
    * `snake_case`: Python, C, Ruby (Funções, Variáveis, Arquivos)
    * `kebab-case`: CSS, HTML (Classes, Arquivos Web)
    * `SCREAMING_SNAKE_CASE`: C, Python (Constantes)
    * Hungarian Notation: C (Tipos em Variáveis)
    * `Flatcase`: URLs curtas
* **Outras Convenções:**
    * Namespaces: Organizar código em módulos (C#). 📂
    * Nomes de Arquivos/Pastas: Regras dos sistemas operacionais (ex: `use_underscores.txt`). 📁
    * Web Naming Conventions: URLs para SEO (ex: `meu-artigo-legal.html`). 🌐

##   Tópico 04: Funções ⚙️

* **O que são Funções?:** Blocos de código para tarefas específicas. [cite: 374, 375]
* **Argumentos vs. Parâmetros:**
    * Argumentos: Valores PASSADOS para a função. ➡️ [cite: 384, 385]
    * Parâmetros: Variáveis que a função RECEBE. ⬅️ [cite: 385]
* **Funções vs. Métodos:**
    * Métodos pertencem a classes/objetos. 🏛️ [cite: 386, 387]
    * Método tem `self` ou `this`. 🙋 [cite: 387]
* **Single Responsibility Principle (SRP):**
    * Cada função deve ter UMA única responsabilidade. ☝️ [cite: 390, 391]
    * Funções grandes devem ser divididas. ✂️
* **Funções Pequenas:** Funções grandes são complexas. 🐘
* **Nomeando Funções:**
    * Use nomes claros e descritivos. 🗣️
    * O nome deve dizer o que a função FAZ. 🎯
* **Argumentos:**
    * Poucos argumentos (0 a 2) são ideais. 🤏
    * Muitos argumentos confundem. 😕
    * Use objetos para agrupar argumentos. 📦
* **Funções Sem Efeitos Colaterais:**
    * A função deve fazer APENAS o que o nome indica. 🧘
    * Evite modificar variáveis externas. ☣️
* **Separação Comando/Consulta:**
    * Funções devem ou responder (consulta) ou alterar (comando), não ambos. ❓ 🔨
* **Prefira Exceções a Códigos de Erro:** Exceções facilitam o tratamento de erros. 🚨 [cite: 1070, 1071]
* **Evite Duplicação:** Código duplicado dificulta a manutenção. 👯

##   Tópico 05: Comentários 💬

* **O Uso de Comentários:** Comentários explicam o código para outros devs. [cite: 516, 517]
* **"Comentários são sempre fracassos."** (Clean Code): O código deve ser autoexplicativo. 😥 [cite: 520, 521, 522]
* **Comentários Não Compensam Código Ruim:** Código limpo precisa de menos comentários. 🌟 [cite: 523, 524]
* **Bons Comentários:**
    * Informações Legais: Licenças, etc. 📜
    * Explicação de Intenção: Por que algo foi feito assim. 🤔
    * Esclarecimento: Código complexo. 🤯
    * Avisos: Para prevenir erros futuros. ⚠️
    * TODOs: Para lembrar de tarefas. 📝
* **Maus Comentários:**
    * Código Supérfluo: Explicar o óbvio. 🤦
    * Comentários Mandatórios: Sem valor real. 🪦
    * Comentários Jornalísticos: Descrever cada linha. 📰
    * Comentários Barulhentos: Poluição visual. 📢
    * Comentários de Fechamento: Para chaves/colchetes. 🧱
    * Atribuição: Quem criou/modificou (o git faz isso!). 👤
    * Comentários Obsoletos: Desatualizados. 🕰️
    * Comentários Redundantes: Repetem o código. 🦜
    * HTML em Comentários: Confuso! 🕸️
    * Informações Não Locais: Contexto irrelevante. 🗺️
    * Comentários Ocultos: Código comentado (use o git!). 👻
* **Posição dos Comentários:** Acima do código que explicam. ⬆️

##   Tópico 06: Estrutura e Formatação 🎨

* **Objetivo da Formatação:** Tornar o código claro e legível. 📖 [cite: 685, 686]
* **Formatação Vertical:**
    * Arquivos curtos são mais fáceis de entender. 🤏 [cite: 689, 690]
    * Use a metáfora do "Jornal": Manchete (nome), Sinopse (início), Detalhes (resto). 📰 [cite: 692, 693, 694]
* **Espaçamento Vertical:**
    * Linhas em branco separam blocos de código. ↔️ [cite: 588, 589]
    * Funções/métodos são separados por linhas em branco. [cite: 589]
* **Formatação Horizontal:**
    * Use espaços para clareza (ex: em atribuições, operadores). ↔️
    * Alinhamento ajuda a visualizar (ex: variáveis). ↕️
* **Indentação:**
    * Mostra a estrutura do código (`if`, `for`, etc.). ↪️
    * Use 2 a 4 espaços (ou tabs) por nível.
* **Tamanho da Linha:**
    * Evite linhas muito longas (use 80-120 caracteres). 📏
    * Quebre linhas longas para facilitar a leitura.
* **Coesão:**
    * Funções devem fazer sentido juntas. 🤝
    * Evite misturar conceitos diferentes. 🍲
* **Ordenação:**
    * Mantenha uma ordem lógica (variáveis, métodos públicos, privados, etc.). 🗂️
* **Escopos Minúsculos:**
    * Blocos pequenos podem ser em uma linha. 🤏
    * Mas cuidado para não exagerar! 🙈
* **Equipes de Formatação:**
    * Estilo de formatação UNIFICADO é essencial. 👯‍♀️

##   Tópico 07: Linters 🤖

* **Style Guides:** Documentos com as convenções de estilo do time. 📜 [cite: 804, 805]
* **Linters:** Ferramentas que verificam se o código segue o Style Guide. ✅
* **Vantagens dos Linters:**
    * Automatizam a verificação de estilo. ⚙️
    * Evitam discussões sobre estilo. ☮️
    * Garantem consistência. 🤝
* **Integração dos Linters:**
    * No IDE (enquanto você codifica). 💻
    * Em pipelines de CI/CD (antes de enviar o código). 🚀
* **Linters Populares:**
    * ESLint e Prettier (JavaScript)
    * Flake8 e Black (Python)
    * Rubocop (Ruby)
    * PHPStan (PHP)
    * SonarLint e Checkstyle (Java)
    * Clang-tidy (C e C++)

##   Tópico 08: Estruturas de Dados 📦

* **Dados:** Podem ser representados de várias formas (structs, classes, arrays). [cite: 888, 889, 890]
* **Abstração de Dados:**
    * Um ponto pode ser representado por coordenadas cartesianas ou polares. 📍 [cite: 891, 892, 893]
    * Abstração permite mudar a representação sem afetar o uso. 🎭 [cite: 894, 895, 896, 897, 898]
* **Anti-simetria Dado/Objeto:**
    * Objetos podem manipular outros ou serem manipulados. 🤝 [cite: 899, 900]
    * Objetos manipulados são "objetos de valor" (ou POJOs). 💎 [cite: 900]
* **Lei de Demeter:**
    * Um objeto só deve interagir com seus "amigos" diretos. 🧑‍🤝‍🧑 [cite: 901]
    * Evite "cadeias de chamadas" longas (`a.getB().getC().getD()`). ⛓️
* **Classes de Transferência de Dados (DTOs):**
    * Objetos para transportar dados entre partes do sistema. 🚚
    * Não devem ter lógica de negócio. 💼
* **Tipos de Dados:**
    * Primitivos: `int`, `float`, `boolean`. 👶
    * Objetos: Instâncias de classes.
* **Estruturas de Dados:**
    * Arrays: Listas ordenadas. 🔢
    * Listas Encadeadas: Elementos ligados entre si. 🔗
    * Pilhas: LIFO (último a entrar, primeiro a sair). 🔝
    * Filas: FIFO (primeiro a entrar, primeiro a sair).  очереди
    * Árvores: Estruturas hierárquicas. 🌳
    * Tabelas Hash: Mapeiam chaves a valores. 🔑
* **Primitivos vs. Objetos:**
    * Primitivos são copiados por valor, objetos por referência. 👯
    * Cuidado com efeitos colaterais ao passar objetos como parâmetros. ☣️

##   Tópico 09: Tratamento de Erros 🚨

* **O que são Exceções?:** Mecanismo para lidar com erros. [cite: 1058, 1059]
* **Exemplo de Tratamento de Exceção:** `try-catch-finally` é comum. [cite: 1060, 1061]
    * `try`: Código que pode dar erro.
    * `catch`: Lida com o erro.
    * `finally`: Sempre executado.
* **Lançamento de Exceções:** Use `throw` ou `raise`. [cite: 1062, 1063]
* **Let It Crash:** Em algumas linguagens (Elixir, Erlang), o programa quebra para se recuperar mais rápido.
