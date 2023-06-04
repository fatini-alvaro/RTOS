# RTOS

## Introdução

Um Sistema Operacional em Tempo Real (RTOS - Real Time Operating System) é um tipo de sistema operacional projetado para lidar com tarefas em tempo real. Ao contrário dos sistemas operacionais convencionais, que podem priorizar a eficiência ou a multitarefa em geral, um RTOS é otimizado para fornecer respostas rápidas e previsíveis a eventos em tempo real.

Um RTOS é projetado para atender aos requisitos de tempo e determinismo de sistemas em tempo real, nos quais a precisão do tempo de resposta é essencial. Esses sistemas são frequentemente encontrados em aplicações como controle industrial, sistemas de automação, dispositivos médicos, sistemas embarcados, veículos autônomos e muitos outros.

O RTOS fornece recursos especiais que permitem o gerenciamento adequado de tarefas em tempo real. Ele oferece serviços de agendamento de tarefas, priorização, comunicação e sincronização entre tarefas, além de fornecer mecanismos para lidar com eventos e interrupções em tempo real.

Uma das características importantes de um RTOS é sua capacidade de garantir prazos de execução. Isso significa que as tarefas em tempo real são executadas dentro de limites de tempo bem definidos e conhecidos. Isso é alcançado por meio de técnicas de agendamento apropriadas, como preempção, priorização e atribuição de recursos.

Além disso, um RTOS pode fornecer recursos de gerenciamento de memória, controle de dispositivos, serviços de comunicação interprocessual e outros recursos comuns encontrados em sistemas operacionais convencionais.

##  Multitarefa com FreeRTOS
O FreeRTOS é um popular sistema operacional de tempo real de código aberto que oferece suporte a multitarefa em sistemas embarcados. Ele fornece um ambiente de execução leve e eficiente para executar várias tarefas concorrentes em um sistema.

Com o FreeRTOS, é possível criar e gerenciar várias tarefas independentes que podem ser executadas simultaneamente ou em paralelo. Cada tarefa é definida como uma função em C e pode ser priorizada de acordo com a importância e a urgência das suas respectivas funcionalidades.

## Sincronização de tarefas
Quando as tarefas não compartilham recursos ou dados entre si. Se cada tarefa tem seu próprio conjunto exclusivo de recursos e não há dependências entre elas, não há necessidade de sincronização.

No entanto, em muitos casos, as tarefas precisam interagir e compartilhar recursos, como acesso a uma área de memória compartilhada, acesso a dispositivos periféricos ou comunicação entre tarefas. Nesses cenários, a sincronização se torna essencial para garantir que as tarefas cooperem corretamente e evitem condições de corrida, onde múltiplas tarefas acessam ou modificam os mesmos recursos simultaneamente, causando resultados imprevisíveis ou incorretos.

Para lidar com a sincronização em um ambiente de produção, são utilizados mecanismos como semáforos e mutexes.

Semáforos: São estruturas de dados que atuam como contadores e são usados para controlar o acesso concorrente a recursos compartilhados. Eles permitem que uma tarefa bloqueie ou aguarde até que um recurso esteja disponível ou até que uma condição específica seja atendida.

Mutexes (Mutual Exclusion): São mecanismos que fornecem exclusão mútua para recursos compartilhados. Apenas uma tarefa por vez pode adquirir o mutex e acessar o recurso protegido por ele. Se outra tarefa tentar adquirir o mesmo mutex, ela será bloqueada até que o mutex seja liberado pela tarefa atual.

Esses mecanismos de sincronização, como semáforos e mutexes, ajudam a evitar problemas de concorrência, garantindo que apenas uma tarefa possa acessar um recurso compartilhado de cada vez. Eles garantem a coerência dos dados e evitam conflitos e condições de corrida.

Em um ambiente de produção, onde várias tarefas estão em execução simultaneamente e compartilham recursos, é importante implementar mecanismos de sincronização adequados para garantir o comportamento correto e previsível do sistema. A escolha entre semáforos, mutexes ou outros mecanismos depende dos requisitos específicos e da natureza da aplicação.
