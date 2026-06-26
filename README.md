Desarrollo de examen Pensamiento Computacional

Se estructuró un modelo de tres estados que controla el flujo de pantallas y un algoritmo que traduce el porcentaje acumulado directamente en el tamaño en píxeles del corazón, haciéndolo crecer de forma proporcional. Además, el programa incluye una mecánica de riesgo basada en probabilidades aleatorias que se activa al superar la meta base: cada pulsación extra aumenta el peligro de reiniciar el sistema por un exceso de volumen, desafiando al usuario a decidir entre seguir arriesgándose o usar un comando de escape seguro para volver al menú de forma controlada.

Link de P5js editable: https://editor.p5js.org/rocio.diaz3/sketches/dE06yuYpk

Link de P5js solo vista: https://editor.p5js.org/rocio.diaz3/full/dE06yuYpk

<img width="595" height="595" alt="image" src="https://github.com/user-attachments/assets/e68c0e88-1c78-4354-a963-a9b1f400cbe3" />

*Pantalla principal. Cuenta con título, intrucciones y un mensaje de "advertencia"*

<img width="595" height="596" alt="image" src="https://github.com/user-attachments/assets/82bd6389-9df5-46df-9652-8648b9874390" />

*Inicio del sistema interactivo, con la pulsación del click el corazón aumenta. Se muestra el porcentaje de "Amor" abajo indicando que tan lleno está.*

<img width="595" height="595" alt="image" src="https://github.com/user-attachments/assets/0459f261-afd1-4e34-be33-a0a775a0bf69" />

*Cuando logras llegar al 100%, puedes elegir retirarte a salvo o arriesgarte a llenarlo más de "Amor"

<img width="597" height="595" alt="image" src="https://github.com/user-attachments/assets/786d016f-3fc7-4223-93c1-ae44ae96efa6" />

"Si pierdas, cuenta con una opción de vovler a la pantalla principal*

PROCESO: 

Estados: Se implementó una máquina de tres estados finitos (estado = 0, 1, 2) controlada mediante condicionales if / else if en el bucle principal. La pantalla de juego activo y una pantalla de derrota.

Inputs y Eventos: Utiliza el evento mousePressed() para iniciar con un clic del ratón, y el evento keyPressed() para capturar la barra espaciadora (keyCode 32), la tecla ENTER (keyCode 13) y la tecla "R".

Procesos: Al presionar espacio, se ejecuta el proceso de aumento. Al superar el umbral del 100%, se activa un proceso de evaluación aleatoria aleatoria (random()) que determina si el sistema se desestabiliza o si permite continuar.

Elementos Multimedia: Se integra el uso de preload() para realizar la carga de un archivo de audio externo (.mp3), asegurando su función en tiempo de ejecución.

Outputs: Un output sonoro mediante la reproducción  del audio con (.play()) y un output visual dinámico a través de la función map(), traduce linealmente el porcentaje de la variable a dimensiones en píxeles para escalar las figuras geométricas en el espacio.

La interfaz desafía al usuario a seguir arriesgándose para alcanzar un mayor porcentaje, o ejecutar un comando de escape seguro (R) para finalizarlo en su estado actual.

BOCETOS INICIALES: 

<img width="586" height="730" alt="image" src="https://github.com/user-attachments/assets/54fedb4b-1213-4b3b-ad25-1a81b5965a5f" />
<img width="779" height="671" alt="image" src="https://github.com/user-attachments/assets/d9a762e8-d375-4132-b6c9-dcea4c2ae3f3" />

La decisión de diseño más relevante fue la implementación  de "riesgo contra recompensa" mediante la tecla **R**. Al permitir que el usuario elija retirarse a salvo tras superar el 100%, el proyecto dejó de ser un contador plano y pasó a ser un juego de estrategia. Asimismo, se optó por recalibrar el algoritmo de aleatoriedad a un 20% de probabilidad de fallo por pulsación.
La mayor complicación técnica que tuve fue implementar el algoritmo de aleatoriedad una vez superado el 100%. Inicialmente, el sistema evaluaba el azar con una probabilidad de fallo muy alta (50% en cada pulsación), lo que provocaba que el juego terminara abruptamente de manera injusta y arruinara la experiencia. Resolver esto requirió  reestructurar las condicionales para acotar el rango numérico para bajar el riesgo a un 20% por intento, y asegurar  que al alcanzar el tope absoluto del 200% la derrota fuera obligatoria.

<img width="513" height="643" alt="image" src="https://github.com/user-attachments/assets/4edded0d-a109-44fc-9ab2-2adbe8e6c95c" />

*Diagrama de flujo*
