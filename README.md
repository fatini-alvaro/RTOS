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

## Reações baseadas em condições de tempo real.
No desafio adicionei duas tarefas a mais, uma que liga e desliga o led a cada meio segundo, nao tem validação para acender o mesmo, no outro adicionei uma validação que verifica o valor da variavel que guarda o valor da temperatura para acender o led.

##Vantagens
O uso de um Sistema Operacional em Tempo Real (RTOS) oferece várias vantagens no desenvolvimento de aplicações para Internet das Coisas (IoT). Aqui estão algumas das principais vantagens do uso de um RTOS em aplicações IoT:

Gerenciamento eficiente de recursos: Um RTOS é projetado para lidar com restrições de recursos, como processamento limitado, memória e energia. Ele oferece um gerenciamento eficiente desses recursos, permitindo que as aplicações IoT sejam executadas de forma otimizada mesmo em dispositivos com recursos limitados.

Multitarefa e responsividade em tempo real: O RTOS permite a execução de várias tarefas de forma concorrente, oferecendo um ambiente de tempo real para aplicações IoT. Isso permite que diferentes partes do sistema funcionem de forma independente, respondendo de maneira rápida e previsível a eventos em tempo real, como a chegada de dados de sensores ou comandos remotos.

Sincronização e comunicação entre tarefas: O RTOS fornece mecanismos de sincronização e comunicação entre tarefas, como semáforos, mutexes e filas. Isso facilita a coordenação entre os diferentes componentes de uma aplicação IoT, permitindo que as tarefas compartilhem informações, acessem recursos compartilhados de forma segura e cooperem em tempo real.

Tolerância a falhas e robustez: O RTOS oferece recursos para lidar com falhas e situações de erro. Com mecanismos como watchdog timers e tratamento de exceções, o RTOS pode detectar e recuperar automaticamente de falhas, garantindo a robustez e confiabilidade das aplicações IoT.

Facilidade de desenvolvimento e portabilidade: Os RTOSs geralmente fornecem uma camada de abstração que simplifica o desenvolvimento de aplicações IoT. Eles oferecem APIs padronizadas, bibliotecas e ferramentas que facilitam o desenvolvimento, depuração e teste de software. Além disso, a portabilidade é uma vantagem, pois os RTOSs são projetados para funcionar em uma ampla variedade de plataformas e dispositivos, permitindo que as aplicações sejam facilmente migradas entre diferentes ambientes.

Escalabilidade e flexibilidade: Os RTOSs são altamente escaláveis, permitindo que as aplicações IoT cresçam e se adaptem às necessidades em constante evolução. Eles suportam a adição de novas funcionalidades e a integração com novos dispositivos ou protocolos, fornecendo flexibilidade para expandir e atualizar as aplicações IoT conforme necessário.

No geral, o uso de um RTOS nas aplicações IoT oferece benefícios significativos, como eficiência no uso de recursos, multitarefa em tempo real, sincronização, tolerância a falhas e facilidade de desenvolvimento. Essas vantagens contribuem para a criação de aplicações IoT robustas, responsivas e escaláveis, permitindo a construção de sistemas inteligentes e conectados com alto desempenho e confiabilidade.
