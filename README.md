# Sonrisa Uruguaya · Asistente virtual

Ejercicio académico de creación y despliegue de un asistente virtual para la clínica dental ficticia **Sonrisa Uruguaya**.

El agente fue configurado en Chatbase para responder consultas administrativas sobre:

- horarios de atención;
- servicios ofrecidos;
- atención de urgencias;
- excepción para urgencias pediátricas de menores de 12 años.

## Tecnologías utilizadas

- **Chatbase:** configuración del agente, instrucciones, fuentes y Help Page.
- **Vercel:** despliegue y proxy de la Help Page bajo un dominio propio de Vercel.

## Funcionamiento

El archivo `vercel.json` utiliza *rewrites* para mostrar la Help Page de Chatbase desde la ruta `/help` sin cambiar la dirección visible en el navegador.

También reenvía los recursos estáticos y las solicitudes del chat necesarias para que el asistente funcione correctamente.

La ruta `/` redirige temporalmente a `/help` para facilitar el acceso a la demostración.

## Despliegue

1. Importar este repositorio como un proyecto nuevo en Vercel.
2. Mantener el directorio raíz y la configuración automática.
3. Ejecutar **Deploy**.
4. Abrir la URL generada. La página principal redirigirá a `/help`.

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
