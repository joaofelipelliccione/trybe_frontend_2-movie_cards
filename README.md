👨‍💻 _[Dê uma olhada em como ficou meu projeto!](https://joaofelipelliccione.github.io/trybe_frontend_2-movie_cards/)_

## Projeto Movie Cards Library Stateful

Foi desenvolvida uma aplicação **React** composta por um `conjunto de componentes` React e controlada por estados.
A aplicação que consiste em uma biblioteca de cartões de filmes dinâmica utilizando React. A biblioteca é composta por:

* Um cabeçalho;

* Uma barra de busca, utilizada pra filtrar quais cartões serão exibidos na lista de cartões;

* Uma lista de cartões, onde cada cartão representa um filme e possui uma imagem, título, subtítulo, sinopse e avaliação;

* Um formulário para adicionar um novo cartão na biblioteca.


### Objetivos do Projeto

  - Ler o estado de um componente e usá-lo para alterar o que exibimos no browser
  - Inicializar um componente, dando a ele um estado pré-definido
  - Atualizar o estado de um componente
  - Capturar eventos utilizando a sintaxe do React
  - Criar formulários utilizando sintaxe JSX com as tags : `input`, `textarea`, `select`, `form`
  - Transmitir informações de componentes filhos para componentes pais via callbacks

### Requisitos do Projeto

  - [1 - Crie um componente chamado `<SearchBar />`](#1---crie-um-componente-chamado-searchbar-)
  - [2 - Renderize um formulário dentro de `<SearchBar />`](#2---renderize-um-formulário-dentro-de-searchbar-)
  - [3 - Renderize um input do tipo texto dentro do formulário em `<SearchBar />`](#3---renderize-um-input-do-tipo-texto-dentro-do-formulário-em-searchbar-)
  - [4 - Renderize um input do tipo checkbox dentro do formulário em `<SearchBar />`](#4---renderize-um-input-do-tipo-checkbox-dentro-do-formulário-em-searchbar-)
  - [5 - Renderize um select dentro do formulário em `<SearchBar />`](#5---renderize-um-select-dentro-do-formulário-em-searchbar-)
  - [6 - Crie um componente chamado `<AddMovie />`](#6---crie-um-componente-chamado-addmovie-)
  - [7 - Renderize um formulário dentro de `<AddMovie />`](#7---renderize-um-formulário-dentro-de-addmovie-)
  - [8 - Renderize um input do tipo texto dentro do formulário em `<AddMovie />` para obter o título do novo filme](#8---renderize-um-input-do-tipo-texto-dentro-do-formulário-em-addmovie--para-obter-o-título-do-novo-filme)
  - [9 - Renderize um input do tipo texto dentro do formulário em `<AddMovie />` para obter o subtítulo do novo filme](#9---renderize-um-input-do-tipo-texto-dentro-do-formulário-em-addmovie--para-obter-o-subtítulo-do-novo-filme)
  - [10 - Renderize um input do tipo texto dentro do formulário em `<AddMovie />` para obter o caminho da imagem do novo filme](#10---renderize-um-input-do-tipo-texto-dentro-do-formulário-em-addmovie--para-obter-o-caminho-da-imagem-do-novo-filme)
  - [11 - Renderize uma `textarea` dentro do formulário em `<AddMovie />` para obter a sinopse do novo filme](#11---renderize-uma-textarea-dentro-do-formulário-em-addmovie--para-obter-a-sinopse-do-novo-filme)
  - [12 - Renderize um `input` do tipo `number` dentro do formulário em `<AddMovie />` para obter a avaliação do novo filme](#12---renderize-um-input-do-tipo-number-dentro-do-formulário-em-addmovie--para-obter-a-avaliação-do-novo-filme)
  - [13 - Renderize um `select` do formulário em `<AddMovie />` para selecionar o gênero do novo filme](#13---renderize-um-select-do-formulário-em-addmovie--para-selecionar-o-gênero-do-novo-filme)
  - [14 - Renderize um botão do formulário em `<AddMovie />` para fazer uso dos dados do novo filme, contidos no estado de `<AddMovie />`](#14---renderize-um-botão-do-formulário-em-addmovie--para-fazer-uso-dos-dados-do-novo-filme-contidos-no-estado-de-addmovie)
  - [15 - Crie um componente chamado `<MovieLibrary />`](#15---crie-um-componente-chamado-movielibrary-)
  - [16 - Configure o estado inicial do componente `<MovieLibrary />`](#16---configure-o-estado-inicial-do-componente-movielibray-)
  - [17 - Renderize `<SearchBar />` dentro de `<MovieLibrary />`](#17---renderize-searchbar-dentro-de-movielibrary-)
  - [18 - Renderize `<MovieList />` dentro de `<MovieLibrary />`](#18---renderize-movielist--dentro-de-movielibrary-)
  - [19 - Renderize `<AddMovie />` dentro de `<MovieLibrary />`](#19---renderize-addmovie-dentro-de-movielibrary-)
  - [20 - Adicione proptypes a todos os componentes](#20---adicione-proptypes-a-todos-os-componentes)



#### 1 - Crie um componente chamado `<SearchBar />`

Esse componente renderizará uma barra com filtros acima da listagem de cartões. Quais cartões serão mostrados no componente `<MovieList />` dependerá dos filtros escolhidos. `<SearchBar />` deve receber como props:

  - `searchText`, uma string
  - `onSearchTextChange`, uma callback
  - `bookmarkedOnly`, um boolean
  - `onBookmarkedChange`, uma callback
  - `selectedGenre`, uma string
  - `onSelectedGenreChange`, uma callback


#### 2 - Renderize um formulário dentro de `<SearchBar />`

Dentro desse formulário haverá campos usados na filtragem de cartões.

- Esse formulário deve apresentar o atributo `data-testid="search-bar-form"`


#### 3 - Renderize um input do tipo texto dentro do formulário em `<SearchBar />`

- O input deve ter uma label associada com o texto: **"Inclui o texto:"**;

- Essa label deve apresentar o atributo `data-testid="text-input-label"`

- A propriedade `value` do input deve receber o valor da prop `searchText`;

- A propriedade `onChange` do input deve receber o valor da prop `onSearchTextChange`.

- Esse input deve apresentar o atributo `data-testid="text-input"`



#### 4 - Renderize um input do tipo checkbox dentro do formulário em `<SearchBar />`

- O input deve ter uma label associada com o texto: **"Mostrar somente favoritos"**;

- Essa label deve apresentar o atributo `data-testid="checkbox-input-label"`

- A propriedade `checked` do input deve receber o valor da prop `bookmarkedOnly`;

- A propriedade `onChange` do input deve receber o valor da prop `onBookmarkedChange`.

- Esse input deve apresentar o atributo `data-testid="checkbox-input"`


#### 5 - Renderize um select dentro do formulário em `<SearchBar />`

- O select deve ter uma label associada com o texto: **"Filtrar por gênero"**;

- Essa label deve apresentar o atributo `data-testid="select-input-label"`

- A propriedade `value` do select deve receber o valor da prop `selectedGenre`;

- A propriedade `onChange` do select deve receber o valor da prop `onSelectedGenreChange`;

- O `select` deve renderizar quatro tags `option`, com as opções de filtragem por gênero, na seguinte ordem:
   - `Todos`, com o valor `""`;
   - `Ação`, com o valor `action`;
   - `Comédia`, com o valor `comedy`;
   - `Suspense`, com o valor `thriller`.

- O select deve apresentar o atributo `data-testid="select-input"`

- Cada `option` deve apresentar o atributo `data-testid="select-option"`


#### 6 - Crie um componente chamado `<AddMovie />`

Esse componente renderizará um formulário que permite adicionar na biblioteca um novo cartão de filme, dadas as seguintes informações do novo filme:

  - subtítulo
  - título
  - caminho da imagem
  - sinopse
  - avaliação
  - gênero

`<AddMovie />` deve receber como prop:

  - `onClick`, uma callback

O componente `<AddMovie />` possui como estado as seguintes propriedades:

  - `subtitle`: guarda o subtítulo preenchido no formulário por quem usa a aplicação;
  - `title`: guarda o título preenchido no formulário por quem usa a aplicação;
  - `imagePath`: guarda o caminho da imagem preenchido no formulário por quem usa a aplicação;
  - `storyline`: guarda a sinopse do filme escrita no formulário por quem usa a aplicação;
  - `rating`: guarda a nota de avaliação dada no formulário por quem usa a aplicação;
  - `genre`: guarda o gênero do filme selecionado no formulário por quem usa a aplicação.

Ou seja, o estado de `<AddMovie />` contém as informações do novo filme que foram inseridas por quem usa a aplicação. O estado inicial do componente `<AddMovie />` deve ser:

  - `subtitle`: '';
  - `title`: '';
  - `imagePath`: '';
  - `storyline`: '';
  - `rating`: 0;
  - `genre`: 'action'.


#### 7 - Renderize um formulário dentro de `<AddMovie />`

Dentro desse formulário haverá campos usados para preencher informações do novo cartão a ser adicionado na biblioteca.



#### 8 - Renderize um input do tipo texto dentro do formulário em `<AddMovie />` para obter o título do novo filme

- O input deve ter uma label associada com o texto: **"Título"**;

- Essa label deve apresentar o atributo `data-testid="title-input-label"`

- O input deve ter seu valor inicial provido pelo estado inicial do componente, via `title`;

- Esse input deve apresentar o atributo `data-testid="title-input"`

- A propriedade `onChange` deve atualizar o estado de `<AddMovie />`, atribuindo a `title` o atual título contido no input.


#### 9 - Renderize um input do tipo texto dentro do formulário em `<AddMovie />` para obter o subtítulo do novo filme

- O input deve ter uma label associada com o texto: **"Subtítulo"**;

- Essa label deve apresentar o atributo `data-testid="subtitle-input-label"`

- O input deve ter seu valor inicial provido pelo estado inicial do componente, via `subtitle`;

- Esse input deve apresentar o atributo `data-testid="subtitle-input"`

- A propriedade `onChange` deve atualizar o estado de `<AddMovie />`, atribuindo a `subtitle` o atual subtítulo contido no input.


#### 10 - Renderize um input do tipo texto dentro do formulário em `<AddMovie />` para obter o caminho da imagem do novo filme

- O input deve ter uma label associada com o texto: **"Imagem"**;

- Essa label deve apresentar o atributo `data-testid="image-input-label"`

- O input deve ter seu valor inicial provido pelo estado inicial do componente, via `imagePath`;

- Esse input deve apresentar o atributo `data-testid="image-input"`

- A propriedade `onChange` deve atualizar o estado de `<AddMovie />`, atribuindo a `imagePath` o atual caminho da imagem contido no input.



#### 11 - Renderize uma `textarea` dentro do formulário em `<AddMovie />` para obter a sinopse do novo filme

- A `textarea` deve ter uma label associada com o texto: **"Sinopse"**;

- Essa label deve apresentar o atributo `data-testid="storyline-input-label"`

- A `textarea` deve ter seu valor inicial provido pelo estado inicial do componente, via `storyline`;

- Essa `textarea` deve apresentar o atributo `data-testid="storyline-input"`

- A propriedade `onChange` deve atualizar o estado de `<AddMovie />`, atribuindo a `storyline` a sinopse atual continda na `textarea`.



#### 12 - Renderize um `input` do tipo `number` dentro do formulário em `<AddMovie />` para obter a avaliação do novo filme

- O `input` deve ter uma label associada com o texto: **"Avaliação"**;

- Essa label deve apresentar o atributo `data-testid="rating-input-label"`

- O `input` deve ter seu valor inicial provido pelo estado inicial do componente, via `rating`;

- Essa `input` deve apresentar o atributo `data-testid="rating-input"`

- A propriedade `onChange` deve atualizar o estado de `<AddMovie />`, atribuindo a `rating` a avaliação atual continda no input.


#### 13 - Renderize um `select` do formulário em `<AddMovie />` para selecionar o gênero do novo filme

- O `select` deve ter uma label associada com o texto: **"Gênero"**;

- Essa label deve apresentar o atributo `data-testid="genre-input-label"`

- O `select` deve ter seu valor inicial provido pelo estado inicial do componente, via `genre`;

- O `select` deve apresentar o atributo `data-testid="genre-input"`

- A propriedade `onChange` deve atualizar o estado de `<AddMovie />`, atribuindo a `genre` o gênero atual selecionado;

- O `select` deve renderizar três tags `option`, com as opções de filtragem por gênero, na seguinte ordem:
   - `Ação`, com o valor `action`;
   - `Comédia`, com o valor `comedy`;
   - `Suspense`, com o valor `thriller`.

- Cada `option` deve conter o atributo `data-testid="genre-option"`



#### 14 - Renderize um botão do formulário em `<AddMovie />` para fazer uso dos dados do novo filme, contidos no estado de `<AddMovie />`

- O botão precisa ter escrito o seguinte texto: **"Adicionar filme"**;

- O botão deve conter o atributo `data-testid="send-button"`

- A propriedade `onClick` do botão invoca uma função definida por você, em `<AddMovie />`, que:
  - Executa a callback passada para o componente `<AddMovie />` via props, chamada `onClick`, que recebe como parâmetro o estado atual de `<AddMovie />`;
  - Reseta o estado de `<AddMovie />`, voltando para o inicial, conforme mencionado anteriormente.



#### 15 - Crie um componente chamado `<MovieLibrary />`

Esse componente renderizará a biblioteca de filmes que renderizará a `searchBar` e o `addMovies` para filtrar por filmes e adicionar um filme à biblioteca respectivamente.

`<MovieLibrary />` deve receber como props:

  - `movies`, um array

#### 16 - Configure o estado inicial do componente `MovieLibray`

O componente `<MovieLibrary />` possui como estado as seguintes propriedades:

  - `searchText`: guarda o texto de busca por filmes;
  - `bookmarkedOnly`: um _boolean_ que guarda se é para filtrar por filmes favoritados ou não;
  - `selectedGenre`: guarda o gênero do filme selecionado para poder fazer a filtragem;
  - `movies`: guarda a lista de filmes.

Ou seja, o estado de `<MovieLibrary />` contém a lista de filmes e os filtros a serem aplicados sobre a listagem.

O estado inicial do componente `<MovieLibrary />` deve ser:

  - `searchText`: '';
  - `bookmarkedOnly`: false;
  - `selectedGenre`: '';
  - `movies`: a lista de filmes passadas pela props `movies`.



#### 17 - Renderize `<SearchBar />` dentro de `<MovieLibrary />`

- `searchText` oriundo do estado de `<MovieLibrary />` deve ser passado para a prop `searchText` de `<SearchBar />`;

- A callback para atualizar o estado de `<MovieLibrary />` em `searchText` precisa ser passada para `<SearchBar />`;

- `bookmarkedOnly` oriundo do estado de `<MovieLibrary />` deve ser passado para a prop `bookmarkedOnly` de `<SearchBar />`;

- A callback para atualizar o estado de `<MovieLibrary />` em `bookmarkedOnly` precisa ser passada para `<SearchBar />`;

- `selectedGenre` oriundo do estado de `<MovieLibrary />` deve ser passado para a prop `selectedGenre` de `<SearchBar />`;

- A callback para atualizar o estado de `<MovieLibrary />` em `selectedGenre` precisa ser passada para `<SearchBar />`.


#### 18 - Renderize `<MovieList />` dentro de `<MovieLibrary />`

- Deve passar para a prop `movies` de `<MovieList />` todos os filmes filtrados;

- Quando o estado para `bookmarkedOnly` é falso, não é alterada a listagem de filmes a ser renderizada;

- Quando o estado para `bookmarkedOnly` é verdadeiro, deve ser renderizado por `<MovieList />` somente filmes favoritados;

- Quando o estado para `selectedGenre` é vazio, não é alterada a listagem de filmes a ser renderizada;

- Quando o estado para `selectedGenre` não é vazio, deve ser renderizado somente filmes com o mesmo gênero;

- Quando o estado para `searchText` é vazio, não é alterada a listagem de filmes a ser renderizada;

- Quando o estado para `searchText` não é vazio, deve ser renderizado por `<MovieList />` filmes que satisfaçam a uma das condições abaixo:
  - Filmes cujo título contém o que está presente em `searchText`, **ou**;
  - Filmes cujo subtítulo contém o que está presente em `searchText`, **ou**;
  - Filmes cuja sinopse contém o que está presente em` searchText`.


#### 19 - Renderize `<AddMovie />` dentro de `<MovieLibrary />`

- A callback que permite adicionar um novo filme ao final da lista precisa ser passada para `<AddMovie />`.


#### 20 - Adicione proptypes a todos os componentes

Todos os componentes que recebem props devem ter suas proptypes corretamente declaradas.

---
