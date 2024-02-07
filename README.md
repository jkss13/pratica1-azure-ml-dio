# Criando um modelo de Previsão com o Azure Machine Learning 🔎

Este projeto foi desenvolvido durante o Bootcamp Microsoft Azure AI Fundamentals da DIO

## ✨ Passo-a-passo
- Criar uma conta no Azure
- Criar um novo recurso através do Azure Machine Learning no marketplace
- Preencher detalhes do recurso, avançar e clicar em "Review + create"
- Após deploy completo, clicar em "Go to resource" e depois 
"Lauch studio"
- Acessar ML automatizado, clicar em "Novo trabalho de ML automatizado" e nomear o trabalho e o experimento
- Selecionar o tipo de tarefa como "Regressão"
- Criar ativo de dados, informando um nome, uma descrição e com o tipo "Tabular"
- Selecionar como fonte de dados "Arquivos da web" e utilizar a url "https://aka.ms/bike-rentals". Informar também que apenas o primeiro arquivo têm cabeçalhos
- Avançar até selecionar os dados e clicar em "Criar"
- Configurar as tarefas: adicionar coluna de destino como "Rentals (integer)" e em configurações adicionais, desmarcar a opção "Explicar melhor modelo e ussar todos os modelos suportados" e selecinar os modelos "RandomForest" e "LightGBM"
- Inserir limites (máx. de avaliações: 3; máx. avaliações simultaneas: 3; máx. nós: 3; limite de pontuação da métrica: 0,085; tempo limite do experimento: 15; tempo limite de iteração: 15; habilitar encerramento antecipado)
- Selecionar "Tipo de validação de treinamento", avançar até enviar o trabalho de treinamento e aguardar (no máx. 15 minutos)
- Validar métricas (acessar e visualizar métricas, como os gráficos que estão comparando o valor previsto com o valor real)
- Clicar na saída, registrar e criar um novo "Ponto de extremidade"

## ✨ JSON
```
{
  "input_data": {
    "columns": [
      "day",
      "mnth",
      "year",
      "season",
      "holiday",
      "weekday",
      "workingday",
      "weathersit",
      "temp",
      "atemp",
      "hum",
      "windspeed"
    ],
    "index": [],
    "data": []
  }
}
```

### Referências
[mslearn-ai-fundamentals (microsoftlearning.github.io)](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/02-content-safety.html)

[mslearn-ai-fundamentals (microsoftlearning.github.io)](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/01-machine-learning.html)
