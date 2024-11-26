# SD-PrioridadeThreadsJava
# Projeto: Controle de Prioridade em Threads no Java

Este projeto demonstra a execução de threads com diferentes prioridades em Java. Utilizamos as classes `Thread` e seus métodos principais para criar dois tipos de threads: **Alta Prioridade** e **Baixa Prioridade**.

## Descrição do Projeto

O programa consiste em:
1. **Classe `BaixaPrioridade`:**
   - Thread configurada para prioridade mínima (`Thread.MIN_PRIORITY`).
   - Exibe mensagens continuamente para demonstrar sua execução.

2. **Classe `AltaPrioridade`:**
   - Thread configurada para prioridade máxima (`Thread.MAX_PRIORITY`).
   - Exibe mensagens intercaladas com pausas de 10ms (`sleep(10)`).

3. **Classe `LancadorPrioridade`:**
   - Inicia e gerencia as threads acima.
   - Utiliza um `ShutdownHook` para garantir a interrupção das threads ao final da execução.

  ## Análise da Execução
Ao executar o programa:

Observa-se que a thread de alta prioridade executa com mais frequência que a de baixa prioridade, conforme esperado.
A pausa (sleep(10)) na thread de alta prioridade permite à de baixa prioridade ganhar tempo de CPU ocasionalmente.
O uso de Thread.currentThread().yield() permite que o lançador finalize sua execução enquanto as threads continuam rodando.
O ShutdownHook é ativado no encerramento do programa para interromper as threads, garantindo uma finalização limpa.
