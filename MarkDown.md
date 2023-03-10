a.	Describe la situación y/o problema a simular

El problema a resolver fue adapatar el juego de "Game of Life" el cual sigue las siguientes reglas:

Cualquier celda viva con menos de dos vecinos vivos muere, debido a la subpoblación.
Cualquier celda viva con dos o tres vecinos vivos sobrevive para la siguiente generación.
Cualquier celda con más de tres vecinos vivos muere, debido a la sobrepoblación.
Cualquier celda muerta con exactamente tres vecinos vivos se convierte en una celda viva, debido a la reproducción.

Nuestro objetivo era cambiar las reglas para representar la cuarentena y como se exparce un virus atraves de una poblacion. 

b.	Describe los agentes involucrados así como sus acciones y percepciones

En la actividad cada celda es un agente differente. El cual puede estar en 3 differentes "estados": muerto, vivo o infectado. Cada agente tiene acceso a ver el estado de sus vecinos en las 8 direcciones. EL final del grid se invierte al otro lado del grid. Estos mismo agentes analizan su alrededor y dependiendo de sus vecinos se decide su siguiente estado. 

c.	Describe cómo interactúan y se comunican dos o más agentes del mismo 

El juego se comporta de la misma manera solamente que en vez de korir por sobrepoblacion cada agente se muere atraves de infeccion. AL principio de la infeccion se asignan una cantidad alateoria de de gente infectada. Cada step los agentes analizan los siguientes datos.

Cualquier celda viva se mantiene viva hasta ser infectada por alguno de sus agentes vecinos. 
Cualquier celda viva tiene una probabilidad de x para ser infectada.(x= cantidad de celdas adyacientes * 5)
Cualquier celda Infectada despues de 7 steps de sobrevivir se convierte en una celda viva
Cualquier celda muerta con exactamente tres vecinos vivos se convierte en una celda viva

d.	Describe el entorno

El entrono es un grid de (x x y) donde cada celda es un agente. Se inicializan todos los agentes en cada una de las celdas y se les asigna un estado alateorio 

e.	Identifica las variables y los parámetros que determinan el funcionamiento del sistema.

self.infected
Nos ayuda a definir si el agente se infecto.

self.next_state
Se usa para definir el siguiente estado del agente.

death
Se usa para definir la probabilida de muerte de un agente. 

infection_probability
Se usa para definir la cantidad de vecinos infectados y calcular las probalidades de infeccion.

quarantine_days
Un contador para sanar a los agentes despues de 7 dias de estar infectados.

f.	Describe el proceso de simulación

La simulacion se corre atraves de steps cada step representando un "Dia". Cada step todos los agentes checan a sus vecinos y actualizan su estado en base a las reglas y las probabilidades obtenidas. Este proceso sigue hasta que la infeccion se erradica totalmente o toda la poblacion se muere.

g.	Discute clara y concisamente los resultados obtenidos

Corriendo varias simulaciones conseguimos los mismos resultados que en el game of life. La infeccion nunca se erradica solamente controla la poblacion y nuevos agentes nacen de nuevo. Conseguimos estabilidad ya que la unica condicion de muerte es morir estravez de la infeccion. No hay metodos de control asi que la infeccion no se controla. En casos poco probables la infeccion se erradica de inmediato ya que se aislan. 

h.	Agrega el link al repositorio.
https://github.com/A01177267/Actividad-Integradora-Modelaci-n-de-Sistemas-Multiagentes-