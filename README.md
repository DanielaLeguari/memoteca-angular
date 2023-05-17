# Projeto Memoteca Angular
### Curso Alura: Aplique os conceitos e desenvolva seu primeiro CRUD

# Índice

 1. [Angular](#angular)
 2. [Como criar uma Aplicacao](#aplicacao)
 3. [Conceito SPA](#spa)
 4. [Componentes Angular](#componentes)
 5. [Property Binding](#property-binding)
 6. [Event Binding](#event-binding)
 7. [Two-way Data Binding](#to-way-data-binding)
 8. [Navegação com roteamento](#router)
 9. [Diretivas](#diretivas)
 10. [](#)
 11. [](#)

<div id='angular'/> 

## Framework Angular

- Estrutura baseada em componentes;
- Coleção de bibliotecas integradas;
- Conjunto de ferramentas;

<div id='aplicacao'/> 

## Criação de uma aplicação

- NodeJS;
- Angular CLI; `npm install -g @angular/cli` ;
- `ng new nome-da-aplicacao` para criar a aplicação;
- Irá aparecer algumas perguntas no terminal, sobre add o arquivo de rotas e CSS;
- O próximo passo para inicializar o projeto é entrar na pasta e rodar `ng serve` ou `ng serve --open`; 
- `ng generate component nome-do-componete` ou `ng g c nome-do-componente` para criar um novo componente;


<div id='spa'/> 

## Aplicação de página Única SPA(Single Page Application)

- Significa que todas as funções de seu aplicativo existem em uma única página HTML. 
- À medida que os usuários acessam os recursos do seu aplicativo, o navegador precisa renderizar apenas as partes que interessam ao usuário, em vez de carregar uma nova página. 
- Esse padrão pode melhorar significativamente a experiência do usuário do seu aplicativo.


<div id='componentes'/> 

## Componentes Angular

- Cada componente criado possui  quatro arquivos sendo:
1. nome-do-arquivo.component.css -> CSS do componente;
2. nome-do-arquivo.component.html -> o template;
3. nome-do-arquivo.component.spec.ts -> arquivo de teste;
4. nome-do-arquivo.component.ts -> lógica typescript;

<div id="property-binding"/>

## Property Binding

- É a associação de dados unidirecional e utilizamos [], para rendenizar o conteúdo, utilizamos o recurso de "Propoerty Binding com interpolação" e utilizamos {{ conteudo }}.


<div id='event-binding'/> 

## Event Binding

- O ´Event Binding´ é um tipo unidirecional de Data Binding (ou associação de dados). Mas enquanto o Property Binding envia dados do component para o template, o Event Binding faz o contrário, envia dados do template para o component;
- O Property Binding usa colchetes [] enquanto o Event Binding usa parênteses ().


<div id='to-way-data-binding'/> 

## Two-way Data Binding

- Em Angular o ("one-way data binding") representa uma via de mão única, enquanto o fluxo bidirecional ("two-way data binding") seria uma via de mão dupla;
- A sintaxe do o fluxo de dados bidirecional é uma junção das duas que vimos antes: colchetes [] e parênteses (), formando assim a famosa banana na caixa.
- Para configurarmos o data binding bidirecional, utilizaremos uma diretiva no input de pensamento do arquivo HTML;
- Utilizamos a diretiva de atributo ngModel, que faz parte do FormsModule;
- Exemplo: [(ngModel)]="pensamento.conteudo";
- A diretivangModel é muito utilizada em formulários justamente pela sua capacidade de realizar uma vinculação bidirecional.


<div id='router'/>


## Navegação com roteamento

- Com o router-outlet, informamos ao Angular que queremos que os componentes sejam carregados dinamicamente. Mas não informamos quais componentes ele deve carregar e em quais momentos eles devem ser carregados.
- Acessando o arquivo app-routing.module.ts, temos a constante `routes` que representa as rotas da aplicação.
- As rotas de uma aplicação são um array (arranjo, em português), pois são múltiplas. Portanto, para cada rota, informaremos um objeto diferente.
- ➡️ Sempre que criamos um path com o caminho vazio, devemos adicionar outra propriedade chamada pathMatch, que possui dois valores: prefix e full. Selecionaremos o full, pois queremos que toda a URL seja considerada. Se o prefix for selecionado, somente o endereço da página inicial (antes da primeira barra) será considerado.


<div id='diretivas'/>


# Diretivas

- `Diretivas de componentes:`usado com um modelo. Esse tipo de diretiva é a mais comum.
- 📌 Ex. <app-listarPensamentos>

- `Diretivas estruturais:`altera o layout do DOM adicionando e removendo elementos DOM.
- 📌 Ex. NgIf, NgFor. NgSwitch.

- `Diretivas de atributos:`altera a aparência ou o comportamento de um elemento, componente ou outra diretiva.
- 📌 Ex. NgClass, NgStyle.