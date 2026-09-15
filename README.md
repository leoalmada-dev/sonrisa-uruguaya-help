# Sonrisa Uruguaya · Asistente virtual

Ejercicio académico de creación y despliegue de un asistente virtual para la clínica dental ficticia **Sonrisa Uruguaya**.

El agente fue configurado en Chatbase para responder consultas administrativas sobre:

- horarios de atención;
- servicios ofrecidos;
- atención de urgencias;
- excepción para urgencias pediátricas de menores de 12 años.

## Tecnologías utilizadas

- **HTML y CSS:** portada pública de la demostración.
- **Chatbase:** configuración del agente, instrucciones, chatbot flotante y Help Page.
- **Vercel:** despliegue del sitio y proxy de la Help Page.

## Funcionamiento

La portada contiene el chatbot flotante de Chatbase y un botón que dirige al centro de ayuda en la ruta `/help`.

El archivo `vercel.json` utiliza *rewrites* para mostrar la Help Page de Chatbase desde esa ruta sin cambiar la dirección visible en el navegador. También reenvía los recursos estáticos y las solicitudes del chat necesarias para que el asistente funcione correctamente.

## Despliegue

1. Importar este repositorio como un proyecto nuevo en Vercel.
2. Mantener el directorio raíz y la configuración automática.
3. Ejecutar **Deploy**.
4. Abrir la URL generada para ver la portada.
5. Usar el botón **Abrir centro de ayuda** para comprobar la ruta `/help`.

No se necesitan variables de entorno, dependencias ni proceso de compilación.

## Pruebas sugeridas

- ¿Qué horario tienen?
- ¿Qué servicios ofrecen?
- ¿Atienden urgencias fuera de horario?
- ¿Atienden urgencias de menores de 12 años?
- ¿Cuál es el número de guardia?

En el último caso, el agente no debe inventar un número si esa información no fue proporcionada.

## Alcance

El asistente cumple una función administrativa y educativa. No realiza diagnósticos, no recomienda tratamientos y no confirma turnos reales.
