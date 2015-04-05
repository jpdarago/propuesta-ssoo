# Propuesta SSOO

Propuesta de organización de la materia Sistemas Operativos para
la Facultad de Ciencias Exactas y Naturales en UBA.

## Objetivo de la materia

Entendiendo al sistema operativo como una API, ver las distintas
posibilidades de uso del mismo y las intricancias necesarias para
desarrollar _software_ de infraestructura a un bajo nivel.

## Temario

* Introducción a UNIX
    * Historia
    * Filosofía:
        * _Todo es un archivo_
        * _Small programs joined by a common interface_
    * Hardware actual a usar
    * GNU, Linux, POSIX
    * Como usar un Shell
    * Utilities básicas: cat, grep, man, ls, ...
* Modelo de proceso
    * Ejecutables
    * Procesos
    * _fork_, _exec_, _wait_,
    * Scheduling
    * _Starvation_, _Priority Inversion_
    * Señales
    * Metodos de IPC
        * Pipes
        * Shared Memory
        * Sockets
    * APIs de inspección de procesos
        * Como funciona strace
        * Como funciona gdb
* Implementando binarios
    * El lenguaje C
    * Concepto de formato de binario: ELF, A.OUT
    * Concepto de linker, loader
    * Pipeline de compilación.
    * Linking Estatico vs Dinamico
    * Modelo de memoria
        * Stack vs Heap vs Segmento de datos
        * API de SO para expansion de memoria
        * Memory allocators: malloc, jemalloc, tcmalloc
* Concurrencia
    * Concurrencia vs Paralelismo
    * Threads vs Proceso
    * Race conditions
    * Semaforos
    * Deadlock y Livelock
    * Amdahl, Scaling y False sharing
        * CPU Bound vs IO Bound vs Memory Bound
    * Usando POSIX Threads para escribir programas concurrentes
    * Otros modelos: monitores, CSP, lock free, transactional memory
* Filesystems
    * API de Filesystem
    * Concepto de Inodos, tipos de archivos
    * Concepto de Virtual File System
    * Una aplicación: Filesystem en la RED
* Drivers
    * Modelo de Driver en Linux
    * Modulos de Kernel
    * Kernel monolitico vs microkernel
    * API de un Driver
* Seguridad Infomatica
    * Isolation de procesos, jailing.
    * Criptografía básica
    * Certificados, PKI, Hashes
    * Randomness en el Kernel
    * Ataques comunes:
        * Buffer Overflow
        * Stack y Heap smashing
        * Brute Forcing y Entropía
    * Como almacenar información de manera segura
* Sistemas distribuidos
    * Modelo de Red
    * Modelo de comunicación: TCP, UDP, RPC
    * Concepto de tiempo y sincronia
    * Algoritmos para sincronizacion, sharing, locking distribuido, etc.
    * Conceptos de userspace:
        * Patrones de Red: Fan In - Fan Out, Pub Sub, etc.
        * Serialización: Protocol Buffers, JSON, ASN.1
        * Modelos de distribucion: MPI, Map Reduce, Spark, ...
* Virtualización
    * Soporte por hardware de virtualizacion
    * Containers en Linux (LHC) + Docker
    * Isolation de procesos
    * Virtualización + Sistemas Distribuidos
        * Amazon Web Services, Docker
        * Cloud infrastructure, Datacenters

## Evaluaciones

2 TPS, 2 Parciales, 4 Talleres

## Talleres

* Linking y Dynamic Loading
* IPC usando pipes y sockets:

    Modelo estilo PHP con programa que lee del Socket, forkea a un binario
    segun path, HTTP basico

* Implementando un filesystem Ext2 pero bien testeado
* Seguridad informatica:

    CTF con 3 niveles mostrando exploits de binarios basicos.
    Potencialmente crackear un binario

## Trabajos Practicos

* Concurrencia usando POSIX Threads:

    Mejorar la performance de un programa serial utilizando todas las
    herramientas disponibles, en particular POSIX Threads.

* Sistemas distribuidos

    Implementar un protocolo de procesamiento de transacciones con locking
    distribuido y medir su performance en requests y mensajes.

    Hacer un reporte de fallas mostrando casos reales de falla del sistema.

## Parciales

Todo lo demas
