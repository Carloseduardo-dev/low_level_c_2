# Validação de CPF e threads em C

Trabalho da disciplina **Programação de Software Básico em C**.

## Objetivo

Demonstrar a validação dos dígitos verificadores de um CPF e a execução de tarefas concorrentes com threads, incluindo a proteção de um contador compartilhado por mutex.

## Compilar e executar no Windows

Com Clang/LLVM-MinGW instalado, execute nesta pasta:

```powershell
clang -std=c11 -Wall -Wextra index.c -o cpf.exe
.\cpf.exe

clang -std=c11 -Wall -Wextra -Wno-unused-parameter threads/index.c -o threads.exe -pthread
.\threads.exe

clang -std=c11 -Wall -Wextra -Wno-unused-parameter threads/mutex.c -o mutex.exe -pthread
.\mutex.exe
```

O programa de CPF lê uma entrada e informa se ela passa pela validação dos dígitos verificadores. O exemplo de threads executa duas tarefas que imprimem os números de 1 a 5; a ordem entre elas pode variar. O exemplo de mutex soma 100.000 incrementos de cada thread e apresenta o contador final igual a 200.000.

Os exemplos que estavam reunidos em `threads/index.c` foram separados em arquivos com um `main` cada. O exemplo adicional `threads/processos.c` utiliza `fork()` e depende de um ambiente Linux/Unix.

## Entrega

- [PDF com os prints de execução e do SAVA](CPF_Threads_SAVA.pdf).
- [Capturas do console](evidencias/).
- [Print fornecido do SAVA](capitulos_sava/print_do_estudo_sava.png).
