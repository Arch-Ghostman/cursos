# **JavaScript**

### **Origem da Linguagem**

 A linguagem JavaScript surgiu em 1995, criada por Brendan Eich, um programador da Netscape Communications. A ideia era desenvolver uma linguagem que permitisse tornar as páginas da web mais interativas, indo além do HTML (estrutura) e do CSS (estilo).

Antes de 1995, os sites eram essencialmente estáticos: construídos apenas com HTML (estrutura) e, um pouco depois, com CSS (estilo). Eles serviam apenas para exibir informações, sem permitir qualquer tipo de interação. Não era possível, por exemplo, clicar em um botão e disparar uma ação programada. A experiência era semelhante a ler um jornal impresso: o leitor apenas consumia o conteúdo, sem poder deixar comentários, curtir uma notícia ou compartilhá-la com outras pessoas.

<img src="https://t.ctcdn.com.br/MQdRFBKgXwmWL_nsP51z_UcOJgk=/640x360/smart/i329497.jpeg" style="border-radius:5px; border: 2px solid"/>

Como podemos observar na imagem acima, o modelo apresentado é de um site de 1993, anterior ao surgimento do JavaScript. Por isso, vemos apenas textos acompanhados de uma imagem ilustrativa. Note também a ausência de botões, pop-ups, cookies ou qualquer outro recurso que exigisse lógica de programação para funcionar.

Diante da necessidade de tornar as páginas web mais interativas — oferecendo ao usuário maior flexibilidade na utilização do conteúdo e ampliando as possibilidades criativas dos desenvolvedores — tornou-se indispensável o surgimento de uma ferramenta capaz de implementar lógica de programação no navegador. Essa ferramenta permitiria que as páginas reagissem às ações do usuário, dando origem a uma nova forma de interação dinâmica na web.

O JavaScript foi pioneiro nessa solução digital, tornando-se até hoje a linguagem de programação mais popular no desenvolvimento web. Mesmo com o surgimento de alternativas que prometem superar suas limitações ou oferecer maior eficiência, o JavaScript continua liderando em popularidade e relevância, sendo a base da maioria dos projetos voltados para a web.

### **Onipresença na Internet?**

Em um cenário hipotético em que o JavaScript deixasse de funcionar ou simplesmente deixasse de existir, é seguro afirmar que grande parte da internet ficaria comprometida. Estima-se que cerca de 90% dos sites modernos dependem dele para oferecer interatividade e dinamismo, o que significaria a paralisação de funcionalidades essenciais. Além disso, muitos aplicativos de celular — que utilizam frameworks baseados em JavaScript — também seriam diretamente afetados, reforçando o quanto essa linguagem é indispensável no ecossistema digital atual.

Embora o JavaScript esteja presente na grande maioria dos sites modernos, cerca de 10% da internet não depende dele. Na maioria das vezes, esses sites são páginas antigas ou legadas, construídas antes da popularização da linguagem, ou mantidas sem atualizações significativas. Também podem incluir sites muito simples, como blogs pessoais, portfólios ou páginas institucionais, que não exigem interatividade avançada. Em alguns casos, a ausência de JavaScript é intencional, visando otimizar o carregamento, a performance ou a compatibilidade com navegadores e dispositivos mais antigos. Esses exemplos mostram que, apesar de essencial para a web moderna, ainda existem nichos onde o JavaScript não é utilizado.

Em resumo a maior parte dos casos. Esses 10% que não usam JavaScript são geralmente:

**1 - Sites antigos ou legados**

* Construídos antes da popularização do JavaScript ou mantidos sem atualização.

* Costumam ser páginas estáticas, basicamente HTML e CSS.

**2 - Sites muito simples ou minimalistas**

* Blogs pessoais, páginas institucionais pequenas ou portfólios que não precisam de interatividade avançada.

**3 - Alguns sites focados em acessibilidade ou performance extrema**

* Existem projetos que optam por não usar JS para garantir carregamento super rápido ou compatibilidade máxima com navegadores antigos ou dispositivos limitados.

### **JavaScript à Frente de Seus Concorrentes** 
Apesar do surgimento de diversas linguagens e frameworks que prometem superar algumas limitações do JavaScript — como TypeScript, Dart, Python (para web via frameworks), ou mesmo WebAssembly para desempenho — nenhuma delas atingiu o nível de popularidade e onipresença do JavaScript. Isso acontece por alguns motivos: primeiro, ele já está profundamente integrado aos navegadores, sendo a única linguagem interpretada nativamente pelo cliente, o que garante compatibilidade imediata sem precisar de plugins ou transpilers. Além disso, seu ecossistema é gigantesco, com milhares de bibliotecas e frameworks que agilizam o desenvolvimento de aplicações complexas. Finalmente, a comunidade é enorme e ativa, oferecendo suporte constante, tutoriais e soluções para praticamente qualquer problema. Por esses fatores, mesmo com alternativas promissoras, o JavaScript continua sendo a escolha predominante no desenvolvimento web moderno, consolidando sua liderança histórica.

## **Características do JavaScript**

### **1 - linguagem de programação dinâmica**
Quando dizemos que o JavaScript é uma linguagem de programação dinâmica, estamos falando sobre a flexibilidade no tempo de execução do código. Vamos detalhar:

Alterações em tempo de execução

Você pode criar, modificar ou remover variáveis, objetos, funções e propriedades enquanto o programa está rodando, sem precisar recompilar nada.

Tipagem dinâmica

Variáveis não têm tipo fixo. Por exemplo, você pode fazer:

```javascript
let valor = 10; // valor é um número
valor = "dez"; // agora valor é uma string
```

Isso torna a programação mais rápida e flexível, mas exige cuidado para evitar erros inesperados.

```javascript
let dado = 10;         // dado é um número
console.log(dado + 5); // 15

dado = "dez";          // agora dado é uma string
console.log(dado + 5); // "dez5" - resultado inesperado para quem esperava soma
```
**Explicação:**

* No primeiro caso, dado + 5 resulta em 15, porque dado é um número.

* No segundo caso, dado se tornou uma string, então dado + 5 concatena a string com o número, produzindo "dez5" em vez de 15.

Isso mostra que a flexibilidade do JavaScript é poderosa, mas exige atenção do programador para evitar resultados inesperados ou bugs.

### **Erros Comuns na Tipagem Dinâmica do JavaScript**

Imagine que você, leitor, está aprendendo JavaScript para adicionar interatividade em seus projetos web, como formulários de cadastro. É importante lembrar que o JavaScript é uma linguagem dinâmica, e isso significa que <strong style="color: rgba(235, 110, 110, 1)">"o tipo de uma variável não é definido quando ela é criada, mas sim quando um valor é atribuído a ela".</strong>

Por exemplo, considere este formulário simples:
```html
<form action='/cadastro' id="cadastroCliente">
  <input type="text" name="nomeCliente" placeholder="Nome do Cliente"/> 
  <input type="text" name="IdadeCliente" placeholder="Idade"/>
  <button>Cadastrar</button>
</form>
```
Se você atribuir um valor numérico a uma variável, o tipo será interpretado como number; se o valor for texto, o tipo será string. No caso do formulário, o campo de idade deveria receber apenas números. Porém, como ele foi definido como 

```html
  <input type="text"/>
``` 
E o JavaScript é dinâmico, o usuário poderia digitar letras ou uma sequência de números no campo errado. Isso faria com que a variável que você esperava ser um número (int) passasse a ser uma string, gerando resultados inesperados em cálculos ou validações.

Esse exemplo mostra que, embora o JavaScript seja poderoso e flexível, é essencial combinar **HTML correto** (usando tipos de input adequados) com **validações em JavaScript**, garantindo que os dados recebidos sejam do tipo esperado e que a aplicação funcione de forma segura e previsível.

📌 **Resumo:** “dinâmica” significa que o comportamento e a estrutura do código podem mudar enquanto o programa está sendo executado, ao contrário de linguagens estáticas, onde tipos e estruturas são definidos e fixos antes da execução.

---

### **2 - Fracamente Tipada**

O JavaScript é considerado fracamente tipado porque ele não exige que você defina o tipo da variável no momento da sua criação. O tipo só é determinado quando um valor é atribuído e pode mudar a qualquer momento, dependendo do novo valor que você colocar nela.

Como mencionado anteriormente, em JavaScript o tipo de uma variável não é definido no momento da sua criação, mas sim no ato da atribuição de um valor. Isso contrasta com linguagens fortemente tipadas, como o Java, onde o tipo é declarado de forma explícita.

**Exemplo em Java:**
```java
  int idade; 
// Mesmo sem receber um valor, a variável já é do tipo inteiro.
``` 
**Exemplo em JavaScript:**
```javascript
let idade; 
// Sem atribuição, a variável permanece indefinida (undefined) e sem tipo fixo.
idade = 25; // Agora ela assume o tipo number
idade = "vinte e cinco"; // Aqui passa a ser string
``` 
📌 **Resumo:** Ou seja, em Java o tipo é fixo e não muda, enquanto em JavaScript ele é dinâmico o valor atribuído é quem define o tipo da variável.

---

### **3 - JavaScript como linguagem interpretada**

O JavaScript é classificado como uma linguagem interpretada, o que significa que seu código não precisa passar por um processo de compilação antes de ser executado. Em vez disso, ele é lido e executado diretamente por um interpretador, geralmente o motor JavaScript presente nos navegadores (como o V8 do Google Chrome ou o SpiderMonkey do Firefox).

Em linguagens compiladas (como C ou Java), o código-fonte precisa ser traduzido para código de máquina antes de rodar, gerando um executável. Já no JavaScript, o código pode ser escrito e executado imediatamente, sem etapas adicionais.

**Exemplo prático**
```javascript
  // Código JavaScript interpretado diretamente pelo navegador
let nome = "Maria";
console.log("Olá, " + nome);
```
Assim que esse código é inserido em um navegador e executado, o motor JavaScript interpreta linha por linha e mostra o resultado no console, sem a necessidade de um arquivo compilado.

### **Vantagens de ser interpretada**
**1 - Rapidez no desenvolvimento**

* Como não há a etapa de compilação, o ciclo “escrever → testar → corrigir” é muito mais ágil. Isso facilita o desenvolvimento web, onde mudanças no código podem ser vistas quase que instantaneamente no navegador.

**2 - Portabilidade**
* O mesmo código JavaScript pode ser executado em diferentes navegadores e sistemas operacionais, sem precisar ser recompilado para cada ambiente.

**3 - Flexibilidade**
* Permite rodar diretamente em navegadores, sem necessidade de instalar compiladores ou ferramentas extras. Basta ter um navegador moderno e o código pode ser testado.

**4 - Menor barreira de entrada**
* Para quem está aprendendo programação, é mais simples escrever um código JavaScript e ver o resultado na hora, comparado com linguagens compiladas que exigem configuração de ambiente e compiladores.

### **Comparação com linguagens compiladas**
**Linguagens compiladas (ex: C, Java, Go)**
* Precisam compilar antes de rodar.
* Costumam ter **melhor performance** porque o código já está traduzido em instruções de máquina.
* Mais seguras em relação a erros de tipagem, já que muitos erros são identificados na etapa de compilação.

**JavaScript (interpretada)**
* **Execução imediata**, sem compilação prévia.
* Mais prática para desenvolvimento rápido e testes.
* enos eficiente em performance bruta que linguagens compiladas, mas compensa em a **gilidade e flexibilidade**.

📌 **Resumo:** O fato de o JavaScript ser **interpretado** é uma das razões pelas quais ele se tornou a principal linguagem da web. Ele permite mudanças rápidas, testes imediatos e portabilidade total entre plataformas. Apesar de linguagens compiladas oferecerem mais desempenho, o JavaScript ganha em **agilidade, simplicidade** e alcance universal.

---
### **Linguagem Baseada em Eventos**
O JavaScript é considerado uma **linguagem baseada em eventos** porque grande parte de sua execução depende da **ocorrência de eventos**.

Um **evento** é qualquer ação que acontece no sistema e que pode ser “ouvida” pelo programa, como:
* um clique do usuário em um botão,

* a digitação de uma tecla,

* o carregamento de uma página,

* a movimentação do mouse,

* ou até a resposta de um servidor.

Em vez de rodar todas as instruções de forma linear e fixa, o JavaScript fica “escutando” os eventos e só executa determinadas funções quando esse evento acontece. Isso torna a linguagem muito flexível e eficiente, principalmente em aplicações interativas.

**Vantagens de ser baseada em eventos**

* **Interatividade:** torna páginas e sistemas mais dinâmicos, respondendo em tempo real às ações do usuário.
 
* **Eficiência**: o código só roda quando necessário, economizando recursos.

 * **Organização:** cada evento pode disparar uma função específica, deixando o código modular.

 **Exemplo prático em JavaScript**
 ```html
 <!DOCTYPE html>
<html>
<head>
  <title>Exemplo de Evento</title>
</head>
<body>
  <button id="meuBotao">Clique aqui</button>
  <p id="mensagem"></p>

  <script>
    // Seleciona o botão
    const botao = document.getElementById("meuBotao");
    const mensagem = document.getElementById("mensagem");

    // Adiciona um "ouvinte de evento" de clique
    botao.addEventListener("click", function() {
      mensagem.textContent = "Você clicou no botão!";
    });
  </script>
</body>
</html>
```
👉 Nesse exemplo, nada acontece até que o **usuário clique no botão**.
Quando o evento de **click** é detectado, a função é executada e a mensagem aparece na tela.

**Comparação com linguagens não baseadas em eventos**

Em algumas linguagens tradicionais, como C ou Java, o código normalmente segue um fluxo sequencial definido pelo programador. Já no JavaScript, o fluxo é reativo, ou seja, o programa responde de acordo com os eventos que acontecem no navegador ou no ambiente em que está sendo executado.

📌 **Resumo:**
JavaScript é considerada uma linguagem baseada em eventos porque sua execução frequentemente depende de ações externas como cliques de mouse, teclas pressionadas ou respostas de servidores. O programa não roda de forma linear e contínua, mas sim aguarda que eventos ocorram e, então, executa funções chamadas event handlers (manipuladores de eventos).