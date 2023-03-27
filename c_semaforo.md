# Concepto de semaforos en sistemas operativos

Un semáforo es un mecanismo de sincronización que se utiliza en los sistemas operativos para controlar el acceso a los recursos compartidos entre procesos o hilos.

Básicamente, un semáforo es una variable entera que puede tomar valores enteros positivos y no negativos. Los procesos pueden realizar operaciones de espera y liberación en los semáforos para asegurar un acceso controlado a los recursos compartidos.

Cuando un proceso desea acceder a un recurso compartido, primero debe hacer una operación de espera en el semáforo asociado a ese recurso. Si el valor del semáforo es positivo, entonces el proceso puede acceder al recurso y el semáforo se decrementa en uno. Si el valor del semáforo es cero, entonces el proceso se bloquea y se coloca en una cola de espera asociada al semáforo.

Cuando un proceso termina de utilizar un recurso compartido, debe hacer una operación de liberación en el semáforo asociado a ese recurso. Esta operación incrementa el valor del semáforo en uno y permite que otro proceso en espera acceda al recurso.

Los semáforos son una herramienta poderosa para la sincronización de procesos y la prevención de condiciones de carrera en los sistemas operativos. Sin embargo, su uso incorrecto puede llevar a problemas de deadlock o inanición.

Un semaforo S es una variable que aparte, de la inicialización, solo se puede acceder por medio de 2 operaciones atómicas y mutuamente exclusivas: 
P=perate                                    V=vete
Whaits(S)                                   Signal(S)
P(S), Down(S)                                v(S), Up(S), Post(S) o Release(S)

Para evitar la espera ocupada: cuando un proceso tiene que esperar, se pondra en una cola de procesos bloqueados esperando un evento.
