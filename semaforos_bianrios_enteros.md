# En qué consisten los semáforos binarios y enteros 

Los semáforos binarios y enteros son dos tipos de semáforos que se utilizan en los sistemas operativos para controlar el acceso a los recursos compartidos.

## Un semáforo binario:
Es un semáforo que solo puede tener dos valores posibles: 0 o 1. Se utiliza para sincronizar procesos que compiten por un recurso único. Por ejemplo, si dos procesos necesitan acceder a una impresora compartida, se puede utilizar un semáforo binario para permitir que solo un proceso acceda a la impresora a la vez.

En un semáforo binario, una operación de espera bloquea un proceso si el valor del semáforo es cero, lo que significa que el recurso está siendo utilizado por otro proceso. Cuando el proceso que está utilizando el recurso libera el semáforo, su valor cambia a 1 y el proceso que estaba esperando se desbloquea y puede acceder al recurso.

## Un semáforo general o entero:
Puede tomar cualquier valor entero positivo o cero. Se utiliza para sincronizar procesos que pueden acceder a varios recursos compartidos. Por ejemplo, si varios procesos necesitan acceder a una piscina de recursos compartidos, se puede utilizar un semáforo entero para limitar el número máximo de procesos que pueden acceder a los recursos al mismo tiempo.

En un semáforo entero, una operación de espera bloquea un proceso si el valor del semáforo es igual a cero. Cuando un proceso libera un recurso compartido, debe hacer una operación de liberación en el semáforo, incrementando su valor en uno. Esto permite que otro proceso en espera acceda a un recurso compartido. El valor del semáforo entero se puede utilizar para controlar el número máximo de procesos que pueden acceder a los recursos compartidos al mismo tiempo.
