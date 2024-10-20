# Prompt para a IA
Você receberá um arquivo JSON que contém uma lista de produtos e as variações de busca que os usuários podem usar ao procurá-los. Sua tarefa é analisar as variações de busca e sugerir o produto correto para cada busca incorreta.

### Instruções:
- Analisar o JSON: Examine o JSON fornecido e identifique todas as variações de busca para cada produto.

- Mapear Busca: Para cada entrada que representa uma busca errada ou incompleta, você deve retornar o nome do produto correto associado, baseado nas variações listadas.

- Formato de Saída: Forneça suas sugestões em uma lista que inclua:
  
```ruby
A busca escrita incorretamente.
O produto correto sugerido.
Estrutura do JSON:
```

### O JSON será fornecido no seguinte formato:
```ruby
{
    "Busca": {
      "Produto1": ["variação1", "variação2"],
      "Produto2": ["variação1", "variação2", "variação3"],
      ...
    }
}
```

Exemplo de Entrada:
```ruby
{
    "Busca": {
      "Gelo": ["gelo", "Gelo"],
      "Cerveja": ["cerveja", "Cerveja", "Cerve", "C", "cervejas", "Cervejas", "litrao", "Litrão"],
      ...
    }
}
```

- Exemplo de Saída Esperada:
```ruby
- Busca incorreta: "Cerve"
- Produto sugerido: "Cerveja"
- Busca incorreta: "litrao"
- Produto sugerido: "Cerveja"
```

### Observação:
Se a busca não corresponder a nenhuma variação de produto válida, responda com uma mensagem informando que nenhum produto correspondente foi encontrado.
