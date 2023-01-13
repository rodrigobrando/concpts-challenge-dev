# Challenge Desenvolvedor Full-Stack JavaScript

## **Descrição**

Em uma aplicação de e-commerce é comum existir sistemas de checkout (carrinho) para que os usuários possam revisar todos os itens, disponibilidade de estoque, descontos, previsão de entrega e frete. Caso todos os produtos estejam disponíveis para compra, deve-se permitir concluir a transação de compra. Levando o usuário para telas de pagamento e registrando um novo pedido de venda na base de dados.

## Critérios de Avaliação

1. TypeScript no Front e Back end.
2. Utilização de padrões de projeto de forma consistente.
3. Padrão RESTful.
4. Utilizar NextJS.
5. Noções básicas de design e construção de interfaces.
6. Modelagem de Banco de Dados.
7. Utilizar Adonis5 JS
8. Utilizar MySql

## **Escopo**

1. Implementar um SPA capaz de listar os produtos e seus respectivos dados.
2. Seguir a ordenação da propriedade _index_.
3. Consultar estoque dos itens do carrinho.
4. O processo de compra somente pode ser concluído caso todos os itens estejam com estoque disponível.
5. Ao clicar em concluir um endpoint de checkout deve ser chamado para registrar o pedido de venda.
6. Tornar possível remover itens do carrinho.
7. Ser possível alterar as quantidades dos produtos.

### **End-points**

Lista de _end-points_ a serem implementados.

#### **Carrinho**

Responsável por retornar dados do carrinho de um usuário.

#### **Mock de resposta**

```
[
  {
    produto: {
      id: 1,
      descricao: 'ALION',
      unidade: 'L',
      volume: 1,
      marca: 'BAYER',
      peso: '1.1KG'
    },
    index: 0,
    quantidade: 10,
    preco: 59.90,
  },
  {
    produto: {
      id: 2,
      descricao: 'VIR CONTROL',
      unidade: 'KG',
      volume: 5,
      marca: 'SIMBIOSE',
      peso: '5.01KG'
    },
    index: 2,
    quantidade: 2,
    preco: 99.90,
  },
  {
    produto: {
      id: 3,
      descricao: 'CURZATE',
      unidade: 'GL',
      volume: 5,
      marca: 'CORTEVA',
      peso: '5.01KG'
    },
    index: 1,
    quantidade: 5,
    preco: 78.95,
  }
  {
    produto: {
      id: 4,
      descricao: 'DMA',
      unidade: 'L',
      volume: 1,
      marca: 'CORTEVA',
      peso: '1.03KG'
    },
    index: 3,
    quantidade: 2,
    preco: 129.90,
  }
]
```

#### **Checkout**

Deve ser chamado para realizar a finalização da compra. E armazenar como um pedido de venda no banco de dados.

#### **Consulta Estoque**

Deve retornar se as quantidades de um produto está disponível no estoque. Deve suportar chamadas recebendo uma lista de produtos. Os dados de entrada devem ser o id do produto e as quantidades selecionadas no carrinho.

- Obs.: Esse end-point não deve retornar dados estáticos, deve consultar alguma fonte a seguinte informação de estoque.

```
[
  produto: {
    id: 1,
    estoque: 5,
  },
  produto: {
    id: 2,
    estoque: 10,
  },
  produto: {
    id: 3,
    estoque: 2,
  },
  produto: {
    id: 4,
    estoque: 0,
  },
]
```

#### **Mock de Resposta**

```
[
  {
    id: 1,
    isDisponivel: true
  },
  {
    id: 2,
    isDisponivel: true
  },
  {
    id: 3,
    isDisponivel: false
  }
  {
    id: 4,
    isDisponivel: false
  }
]
```

### Pontos Extras

1. Chakra UI.
2. React-Query.
3. Implementar alguma solução de cache para disponibilidade estoque.


### Como submeter

- Criar um repositório no GitHub contendo instruções de como executar a aplicação.
- Compartilhar o repositório com os usuários [@RodrigoBrando](https://github.com/rodrigobrando) e [@DiegoSouza7](https://github.com/DiegoSouza7)
- Caso tenha alguma dúvida só chamar
