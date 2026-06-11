Justificación de los 4 factores elegidos
Como parte de mi proceso de aprendizaje en esta etapa de All Star, he analizado la metodología 12-Factor App con el fin de optimizar nuestros flujos de trabajo actuales. He seleccionado estos cuatro pilares porque, al combinarlos con las herramientas que estamos utilizando (Docker y Git), nos permiten pasar de una programación funcional a un despliegue profesional y robusto.

1. Config (Configuración)
Elegí este factor porque es la clave para la portabilidad. En lugar de quemar credenciales o configuraciones dentro del código (lo cual es un riesgo de seguridad y una traba al desplegar), centralizarlas en el entorno me permite que la aplicación sea agnóstica al lugar donde corre. Esto es vital para que podamos mover proyectos de nuestras máquinas locales a cualquier servidor de la organización sin tener que editar ni una sola línea de código.

2. Backing Services (Servicios de apoyo)
Lo seleccioné porque representa la libertad de escalar. Tratar servicios como bases de datos o sistemas de caché como "recursos adjuntos" (conectados mediante URLs/credenciales) nos permite cambiar la infraestructura subyacente sin detener la aplicación. Si mañana necesitamos cambiar de una base de datos local a una en la nube (AWS), la app ni se entera, lo que hace que nuestro trabajo sea mucho más modular y fácil de mantener.

3. Disposability (Desechabilidad)
Me parece fundamental para la estabilidad del equipo. Una aplicación que arranca rápido y se apaga de forma controlada (graceful shutdown) es una aplicación que permite despliegues continuos sin interrupciones. En un entorno de desarrollo activo, esto nos permite reiniciar contenedores ante errores o actualizaciones en cuestión de segundos, reduciendo al máximo cualquier tiempo de inactividad.

4. Dev/Prod Parity (Paridad entre desarrollo y producción)
Lo elegí porque es el remedio definitivo contra el clásico "en mi máquina sí funcionaba". Al usar Docker para mantener la paridad, nos aseguramos de que el código, las dependencias y el entorno sean idénticos en todas las etapas. Esto acorta drásticamente el ciclo de feedback y asegura que, cuando hagamos el push a los repositorios de GitHub de la organización, el despliegue sea predecible y exitoso.
