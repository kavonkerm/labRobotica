# Laboratorio 1 de Robótica y Sistemas Autónomos - ICI4150

## Repositorio para el desarrollo y documentación de los laboratorios del curso Robótica y Sistemas Autónomos (ICI4150) de la PUCV, semestre 2025-01.

### Integrantes del grupo
- Patricio Figueroa
- Marcelo Flores
- Kavon Kermani
- Gabriel Sanzana
- Lucas Zamora

### Ensamblaje y programación de un robot básico

## Herramientas a utilizar 

- Arduino UNO
- Sensores: ultrasónico (HC-SR04) e IMU (MPU6050)
- Driver de motores L298N
- Chasis impreso en 3D con motores DC
- Protoboard y cables de conexión
  
  ****
  
## Parte 1: Identificación de componentes y configuración

• Conectar Arduino UNO con el driver de motores y programar el movimiento básico de los motores (adelante, atrás, giro) sin controlar la
velocidad.
• Verificar el funcionamiento del sensor ultrasónico HC-SR04 midiendo
distancias.
• Analizar los datos del IMU MPUC6050 para medir inclinación o giros
del robot.

## Videos de Demonstración

Poner video 1
Explicar que el video solo esta conectado al motor y que funciona mal , ya que no es posible ir en linea recta y es dificil ir a la izquierda o la derecha, se puede arreglar con el sensor MPU, tampoco esta funcionando el sensor ultrasonido por lo que se va a chocar.

Poner video 2 prueba de sensor ultrasonido
Explicar que el sensor ahora detecta la distancia por que lo va a detectar colisiones.

Poner video 3 prueba de sensor MPU
Explicar que el sensor ahora detecta aceleracion y giro, son datos sin analizar y sin calibrar (detecta acc de gravedad).

## Preguntas

1. ¿Qué función cumplen los sensores, actuadores y controladores en el robot?
Sensores: Capturan información del entorno. Por ejemplo, el HC-SR04 mide la distancia a obstáculos y el MPU6050 detecta inclinaciones o giros del robot.

- Actuadores: Son los dispositivos que ejecutan acciones físicas. En este caso, los motores mueven las ruedas del robot.

- Controladores: Procesan la información de los sensores y toman decisiones para enviar señales a los actuadores. El Arduino UNO actúa como el cerebro del sistema.

2. ¿Cómo se puede estimar la velocidad sin encoders?
Se puede estimar la velocidad midiendo el tiempo que tarda el robot en recorrer una distancia conocida. Por ejemplo, si se sabe que el robot recorrió 50 cm en 5 segundos, su velocidad es de 10 cm/s. Esta estimación puede hacerse combinando temporizadores con sensores como el ultrasónico o simplemente con tiempos programados.

3. ¿Cómo afecta la falta de encoders a la precisión del movimiento?
La ausencia de encoders reduce significativamente la precisión del movimiento. Los encoders permiten un control en tiempo real de la velocidad y posición de las ruedas. Sin ellos, el robot depende de tiempos estimados y puede desviarse fácilmente, especialmente si hay diferencias en los motores o fricción desigual.

4. ¿Qué es PWM y cómo ayuda a controlar la velocidad de los motores?
PWM (Modulación por Ancho de Pulso) es una técnica para controlar la energía promedio entregada a un motor. En lugar de cambiar el voltaje, se enciende y apaga rápidamente el suministro eléctrico. Al variar el "ancho" del pulso (duty cycle), se ajusta la velocidad del motor de manera eficiente y precisa.

5. ¿Cómo afecta el control de velocidad a la precisión de la navegación sin encoders?
El control de velocidad usando PWM mejora la navegación incluso sin encoders, ya que permite equilibrar la velocidad de ambos motores, reduciendo desviaciones. Sin embargo, al no tener retroalimentación real de la posición, sigue existiendo un margen de error, especialmente en trayectorias largas o en condiciones variables (batería baja, peso desigual, etc.).

## Parte 2: Cinemática y Dinámica de Robots Móviles Usando un IMU

• Aplicar la ecuación de cinemática diferencial para estimar la posición del robot usando tiempo y velocidad de motores.

• Hacer que el robot se mueva en línea recta y registrar desviaciones usando el sensor IMU para detectar la inclinación y giro del robot.

• Usar el sensor IMU MPU6050 para medir la inclinación del robot y ajustar su dirección en tiempo real, realizando correcciones en el movimiento de acuerdo a su orientación

• Programar el PWM para controlar la velocidad de los motores y hacer que el robot se mueva a diferentes velocidades sin IMU, variando el tiempo de activación de los motores.

## Preguntas

1. ¿Cómo se calcula la velocidad del robot sin encoders usando PWM?

2. ¿Cómo factores afectan la trayectoria y velocidad del robot al cambiar los intervalos de tiempo?

3. ¿Cuáles son las ventajas y desventajas de usar un IMU para ajustar la dirección en lugar de encoders?

4. ¿Qué efecto tiene la inclinación o el giro en el movimiento del robot, y cómo se corrige con el IMU?




