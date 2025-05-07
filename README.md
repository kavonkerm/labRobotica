1. ¿Qué función cumplen los sensores, actuadores y controladores en el robot?
Sensores: Capturan información del entorno. Por ejemplo, el HC-SR04 mide la distancia a obstáculos y el MPU6050 detecta inclinaciones o giros del robot.

Actuadores: Son los dispositivos que ejecutan acciones físicas. En este caso, los motores mueven las ruedas del robot.

Controladores: Procesan la información de los sensores y toman decisiones para enviar señales a los actuadores. El Arduino UNO actúa como el cerebro del sistema.

2. ¿Cómo se puede estimar la velocidad sin encoders?
Se puede estimar la velocidad midiendo el tiempo que tarda el robot en recorrer una distancia conocida. Por ejemplo, si se sabe que el robot recorrió 50 cm en 5 segundos, su velocidad es de 10 cm/s. Esta estimación puede hacerse combinando temporizadores con sensores como el ultrasónico o simplemente con tiempos programados.

3. ¿Cómo afecta la falta de encoders a la precisión del movimiento?
La ausencia de encoders reduce significativamente la precisión del movimiento. Los encoders permiten un control en tiempo real de la velocidad y posición de las ruedas. Sin ellos, el robot depende de tiempos estimados y puede desviarse fácilmente, especialmente si hay diferencias en los motores o fricción desigual.

4. ¿Qué es PWM y cómo ayuda a controlar la velocidad de los motores?
PWM (Modulación por Ancho de Pulso) es una técnica para controlar la energía promedio entregada a un motor. En lugar de cambiar el voltaje, se enciende y apaga rápidamente el suministro eléctrico. Al variar el "ancho" del pulso (duty cycle), se ajusta la velocidad del motor de manera eficiente y precisa.

5. ¿Cómo afecta el control de velocidad a la precisión de la navegación sin encoders?
El control de velocidad usando PWM mejora la navegación incluso sin encoders, ya que permite equilibrar la velocidad de ambos motores, reduciendo desviaciones. Sin embargo, al no tener retroalimentación real de la posición, sigue existiendo un margen de error, especialmente en trayectorias largas o en condiciones variables (batería baja, peso desigual, etc.).


Poner video 1
Explicar que el video solo esta conectado al motor y que funciona mal , ya que no es posible ir en linea recta y es dificil ir a la izquierda o la derecha, se puede arreglar con el sensor MPU, tampoco esta funcionando el sensor ultrasonido por lo que se va a chocar.

Poner video 2 prueba de sensor ultrasonido
Explicar que el sensor ahora detecta la distancia por que lo va a detectar colisiones.

Poner video 3 prueba de sensor MPU
Explicar que el sensor ahora detecta aceleracion y giro, son datos sin analizar y sin calibrar (detecta acc de gravedad).
