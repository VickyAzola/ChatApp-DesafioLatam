# Chat Mazinger

## Tabla de Contenidos

- [Descripción](#descripción)
- [Características](#características)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Tecnologías Utilizadas](#tecnologías-utilizadas)
- [Instalación](#instalación)
- [Autores](#autores)

## Descripción

Chat Mazinger es una aplicación simple de chat donde se visualizan dos perfiles de usuario obtenidos aleatoriamente mediante una API y permite el envío de mensajes entre ellos. La interfaz del chat muestra los mensajes y permite diferenciarlos según el perfil del usuario que los envía.

![preview](https://github.com/user-attachments/assets/b322a9e8-43fd-4bfa-bdf4-4b3403494a15)


## Características

- Dos perfiles de usuario generados aleatoriamente usando la API de `https://randomuser.me`.
- Componente de chat que muestra los mensajes enviados por cada usuario.
- Los mensajes enviados por el usuario del perfil derecho se alinean a la derecha, mientras que los mensajes del usuario izquierdo se alinean a la izquierda.
- Soporte para cambiar el color de fondo de los mensajes mediante un input de selección de color.

## Estructura del Proyecto

El proyecto está dividido en los siguientes componentes:

1. **MessageApp.vue**: Componente principal que gestiona los perfiles de usuario y los mensajes enviados.
2. **UserCard.vue**: Componente que muestra la tarjeta del usuario, permite escribir mensajes y seleccionar el color del mensaje.
3. **ChatComponent.vue**: Componente que renderiza los mensajes enviados entre los usuarios.

## Tecnologías Utilizadas

- **HTML5**: Para la estructura del sitio web.
- **CSS**: Para el diseño y la presentación del sitio web.
- **Vue.js**: Framework de JavaScript para construir interfaces de usuario.
- **Axios**: Librería para realizar solicitudes HTTP, utilizada para obtener los datos de usuario.
- **API**: API pública de `https://randomuser.me` para generar perfiles de usuario aleatorios. 

## Instalación

Sigue los siguientes pasos para instalar y ejecutar el proyecto en tu entorno local:

1. Clona el repositorio:

    ```bash
    git clone https://github.com/VickyAzola/ChatApp-DesafioLatam.git
    ```

2. Navega al directorio del proyecto:

    ```bash
    cd ChatApp-DesafioLatam
    ```

3. Instala las dependencias necesarias:

    ```bash
    npm install
    ```

4. Inicia el servidor de desarrollo:

    ```bash
    npm run dev
    ```

5.Abre el enlace 'Local' en tu navegador para ver la aplicación en funcionamiento.

## Autores

- **Desarrollador Principal**: [Victoria Azola Silva](https://github.com/VickyAzola) - Responsable del desarrollo del código.
- **Diseñador**: [Desafío Latam](https://desafiolatam.com/admision/?utm_term=desafio%20latam&utm_campaign=Brand&utm_source=adwords&utm_medium=ppc&hsa_acc=1239562006&hsa_cam=16998643182&hsa_grp=136655824715&hsa_ad=596057942540&hsa_src=g&hsa_tgt=kwd-340546658839&hsa_kw=desafio%20latam&hsa_mt=b&hsa_net=adwords&hsa_ver=3&gad_source=1&gclid=CjwKCAjwvvmzBhA2EiwAtHVrbzEJGJPqUuTuFDuNIFtSh4eKqGXcLXmCO9u12vwlU553fGXV93Q5zxoCGmEQAvD_BwE) - Responsable del diseño gráfico y visual del proyecto.
