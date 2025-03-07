27 / 02 / 2025
# Introducción a Simscape Multibody

Simscape Multibody es una herramienta de MATLAB/Simulink que permite modelar, simular y analizar sistemas mecánicos multicuerpo, facilitando la representación gráfica y la simuolación de la dinámica y cinemática de cuerpos rígidos con juntas o articulaciones, actuadores y restricciones, haciendolo un programa ideal para aplicaciones de robótica [1]. Permite modelar sistemas mecánicos 3D, como robots, maquinaria pesada, vehículos, etc.

¿Qué ofrece Simscape mUltibody?
Simscape se encarga de formular y resolver las ecuaciones diferenciales que modelan el comportamiento dinámico de los sistemas físicos, incluyendo las ecuaciones cimenáticas. Permite observar la respuesta temporal de cada variable durante la simulación, proporcionando una representación detallada del sistema.

Además, genera  una animación 3D que muestra el comportamiento a lo largo de toda la dinámica, permitiendo visualizar la evolución del sistema en cada instante de tiempo.


### Ventajas
1. Permite la simulación de diversos sistemas físicos, como sistemas hidráulicos, eléctricos y neumáticos.
2. Facilita la integración de la parte mecánica, el actuador y el controlador dentro del mismo entorno de simulación.
3. Proporciona herramientas eficaces para el analisis y validación de diseños antes de la implementación física.
4. Mejora la comprensión del comportamiento dinámico del sistema a través de representaciones gráficas y animaciones.


💡**Ejemplo 1 - Péndulo Simple** 

##### <------------  IMAGEN DEL PENDULO EN SIMULINK   ----------------->

Se pueden generar todos los solidos y restricciones que requiere el mecanismo. En el ejemplo 1 se definio como restricción de movimiento la rotación del objeto, obteniendo el movimiento de pendulo. Tambien se le puede programar gravedad, esta forma no se requiere de una entrada al pendulo.


##### <------------ IMAGEN DEL SCOPE DEL PENDULO EN SIMULINK  ----------------->

Al analizar la señal resultante se observa que la configuración de simulación influye en la gráfica, por eso se generar picos en los máximos y minimos.



ODE23t


### Diferencias con el software CAD
En el software CAD se pueden hacer modelamientos y simulaciones en temas de esfuerzo, tipo de material, copmortamiento a nivel estructural respecto a difernetes fuerzas, pero lo que no se puede ver en este tipo de sofwate es la dinamica del sistema, ver a nivel de movimiento que esta ocurriendo en terminos de fuerza, velocidad. No se puede graficar una curva de como varia la posición respecto al tiempo o la velocidad respecto al tiempo.





![Figura de prueba](Solver_SC.PNG)

Figura 1. Figura de prueba




# Conclusiones
1. La señal sinusoidal observada está influenciada por la configuración del simulador. Para mejorar su calida, es necesario configurar los tiempos de muestreo con los que se generan las soluciones, así como seleccionar el método de integración más adecuado.
2. La fluidez del movimiento depende de la cantidad de puntos de solución generados. Un mayor número sw puntos permite una representación más continua, evitando la pérdida de información.
3. Cada algoritmo de integración está optimizado para determinadad condiciones, como la frecuencia de respuesta de la integral o cambios no periódicos en la señal, lo que garantiza una mejor precisión en la simulación.
4. La reducción del tiempo de muestreo permite considerar un mayor número de puntos en los cálculos, lo que incrementa la precisión del análisis, pero también conlleva un mayor consumo de recursos computacionales.





# Referencias
1. SimScape Multibody. (s. f.). https://la.mathworks.com/products/simscape-multibody.html
2. “Login aulas 2025”, Edu.co. [En línea]. Disponible en: https://aulas.ecci.edu.co/mod/resource/view.php?id=217529&forceview=1. [Consultado: 11-feb-2025].
