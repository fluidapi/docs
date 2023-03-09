# Espera

O conector de Espera (_wait_) é usado para criar um intervalo de tempo entre um passo e outro durante a execução do seu fluxo.

O conector pode ser usado para 

## Configuração

As duas configurações necessárias indicam a quantidade de tempo que o passo de espera ficará parado aguardando retomar a execução.

Combinadas irão gerar valores como:

- 500ms (milissegundos)
- 10s (segundos)
- 1m (minuto)

São elas:

### Duração

Um número inteiro indicando a quantidade de tempo que o fluxo ficará aguardando antes de retomar a execução.

### Unidade de tempo

Define a unidade de tempo da duração configurada acima.

Os possíveis valores são:

- Milissegundos
- Segundos
- Minutos

## Casos de uso

Um exemplo de caso de uso para este conector é para contornar erros de _rate limit_ (como HTTP _429 Too Many Requests_), onde muitas requisições num curto espaço de tempo são bloqueadas pelo servidor.

Nesses casos onde a execução de dois ou mais passos (requisições) muito próximos um do outro é um problema, inserir o conector de Espera pode ser a solução.
