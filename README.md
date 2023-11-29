# Jogo da Velha em React

Este código implementa um jogo da velha (Tic-Tac-Toe) em React. Consiste em três componentes principais:

## Componente `Square`

Representa um quadrado clicável no tabuleiro do jogo.

```jsx
function Square(props) {
  return (
    <button className="square" onClick={props.onClick}>
      {props.value}
    </button>
  );
}

```

## Componente `Board`

Representa o tabuleiro do jogo, contendo 9 quadrados.

```jsx
class Board extends React.Component {
  renderSquare(i) {
    return (
      <Square
        value={this.props.squares[i]}
        onClick={() => this.props.onClick(i)}
      />
    );
  }

  render() {
    // Renderiza os quadrados em linhas
  }
}

```

## Componente `Game`

Controla o estado do jogo, gerencia o histórico de movimentos e identifica o vencedor.

```jsx
class Game extends React.Component {
  constructor(props) {
    // Inicializa o estado do jogo
  }

  handleClick(i) {
    // Manipula os cliques nos quadrados
  }

  jumpTo(step) {
    // Volta para um movimento específico
  }

  render() {
    // Renderiza o tabuleiro, controla o histórico de movimentos e exibe o vencedor ou próximo jogador
  }
}

```

O jogo utiliza estados para controlar o histórico de movimentos, identificar o próximo jogador e determinar o vencedor. Cada vez que um quadrado é clicado, o estado é atualizado para refletir a mudança no tabuleiro.

## Função calculateWinner

Verifica se há um vencedor com base nos quadrados preenchidos.

```jsx
function calculateWinner(squares) {
  // Verifica as linhas, colunas e diagonais para determinar o vencedor
}
```


## Inicialização do Jogo

No final do código, o componente Game é renderizado no elemento com o ID "root" usando ReactDOM.

```jsx
const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(<Game />);
```

Esse é o funcionamento geral do jogo da velha em React. Os componentes Square, Board e Game interagem para proporcionar a funcionalidade completa do jogo.