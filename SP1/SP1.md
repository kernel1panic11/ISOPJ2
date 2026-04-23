---
layout: default
title: "Sprint 1. Instalación y configuración inicial de Windows en máquina virtual"
---

<main class="contenedor-principal">
    <h1 class="titulo">Sprint 1. Instalación y configuración inicial de Windows en máquina virtual</h1>
    <div class="loading-bar"><div class="loading-progress"></div></div>

    <div class="navigation-links">
        <a href="{{ '/' | relative_url }}"><i class="fa-solid fa-house"></i> Volver al inicio</a>
        <a href="{{ '/SP2/SP2.html' | relative_url }}">Siguiente práctica <i class="fa-solid fa-arrow-right"></i></a>
    </div>

    <div class="content-section">
        <h2 class="sub">Enfoque del sprint</h2>
        <p>
            Este sprint se centra en la instalación y configuración inicial de <strong>Windows 11</strong> dentro de una máquina virtual, siguiendo un proceso ordenado que permita dejar el sistema operativo correctamente implantado, configurado y listo para su uso. No se trata solo de completar la instalación, sino de entender qué se está haciendo en cada fase y justificar técnicamente las decisiones tomadas.
        </p>
        <p>
            Además de instalar el sistema, será necesario documentar el proceso con capturas de pantalla colocadas en el punto exacto donde se explica cada acción. De este modo, la práctica no solo muestra el resultado final, sino también la evidencia visual de cada paso importante: creación de la máquina virtual, instalación del sistema, activación, red, software base y comprobaciones de arranque.
        </p>
    </div>

    <div class="content-section">
        <h2 class="sub">Objetivos del Sprint 1</h2>
        <ul>
            <li>Instalar Windows 11 en una máquina virtual correctamente configurada.</li>
            <li>Realizar la configuración inicial del sistema para dejarlo operativo.</li>
            <li>Comprobar la conectividad de red y la configuración IP del entorno virtual.</li>
            <li>Verificar el estado de activación y justificar el tipo de licencia más adecuado.</li>
            <li>Instalar software base y validar su funcionamiento.</li>
            <li>Analizar aspectos básicos del arranque y de la recuperación del sistema.</li>
            <li>Documentar todo el procedimiento con explicaciones breves y capturas relevantes.</li>
        </ul>
    </div>

    <div class="content-section">
        <h2 class="sub">Fase 1. Preparación de la máquina virtual</h2>

        <h3>Paso 1. Crear la máquina virtual</h3>
        <p>
            Se crea una máquina virtual en <strong>VMware</strong> destinada a alojar <strong>Windows 11</strong>. En este paso debe indicarse el nombre de la máquina, el tipo de sistema operativo seleccionado y el hecho de que se está preparando un entorno aislado para realizar toda la práctica sin afectar al equipo anfitrión.
        </p>
        <p>
            A continuación se muestran las capturas del asistente de creación de la máquina virtual en VMware, donde se puede ver la selección de la ISO de Windows 11 y la ruta de almacenamiento elegida para el archivo de la máquina virtual.
        </p>
        <div class="capture-placeholder">
            <img width="778" height="479" alt="Creación de la máquina virtual en VMware, selección de ISO" src="https://github.com/user-attachments/assets/0b82925d-74d4-47c3-8622-e07fcc8f4eab" />
        </div>
        <div class="capture-placeholder">
            <img width="765" height="281" alt="Selección de la ubicación donde se guardará la máquina virtual" src="https://github.com/user-attachments/assets/81b6c8f7-7939-406e-8d6f-db317fd86cf4" />
        </div>

        <h3>Paso 2. Asignar recursos de hardware virtual</h3>
        <p>
            A continuación se configura el hardware virtual de la máquina. Se recomienda asignar como mínimo <strong>4 GB de memoria RAM</strong> y un disco virtual de <strong>40 GB</strong>, ya que estos valores permiten instalar Windows 11 con un margen razonable para tareas básicas de ofimática, navegación y trabajo colaborativo.
        </p>
        <p>
            La siguiente captura muestra la pantalla de configuración de hardware de VMware, donde se pueden ver los parámetros asignados a la máquina virtual antes de iniciar la instalación.
        </p>
        <div class="capture-placeholder">
            <img width="820" height="420" alt="Configuración de hardware virtual: memoria, disco y procesadores en VMware" src="https://github.com/user-attachments/assets/84cd15fe-92f5-44ca-a90d-78b2cbf78c58" />
        </div>

        <h3>Paso 3. Cargar la ISO de Windows 11</h3>
        <p>
            Una vez creada la máquina virtual, se asocia la imagen ISO de Windows 11 a la unidad virtual correspondiente para que el sistema pueda arrancar desde ella e iniciar el asistente de instalación. La ISO seleccionada corresponde a <strong>Windows 11 Pro N</strong>, la edición sin aplicaciones multimedia de Microsoft, cuya existencia responde a la normativa europea de competencia que obliga a ofrecer versiones del sistema sin software propietario preinstalado.
        </p>
        <p>
            La captura siguiente muestra la configuración general de la máquina en VMware, confirmando que la ISO queda asociada al dispositivo CD/DVD virtual antes del primer arranque.
        </p>
        <div class="capture-placeholder">
            <img width="843" height="388" alt="Resumen de configuración de la máquina virtual en VMware con ISO cargada" src="https://github.com/user-attachments/assets/9f0247ef-c47d-42cf-9d0e-f115228fd3e0" />
        </div>

        <h3>Paso 4. Justificar la configuración elegida</h3>
        <p>
            En este punto se debe explicar por qué la configuración seleccionada resulta adecuada para el entorno de trabajo planteado. Asignar una cantidad razonable de memoria, un disco suficiente y una red funcional permite instalar y usar Windows 11 con estabilidad, manteniendo además un equilibrio con los recursos disponibles en el equipo anfitrión. La elección de <strong>Windows 11 Pro N</strong> se justifica por el contexto académico europeo: esta edición cumple con la normativa de la UE y permite trabajar con el sistema operativo sin dependencias de software multimedia de terceros.
        </p>
        <p>
            La siguiente captura muestra el asistente de instalación de Windows en el momento de seleccionar la edición del sistema, donde se confirma la elección de Pro N.
        </p>
        <div class="capture-placeholder">
            <img width="753" height="534" alt="Selección de Windows 11 Pro N durante la instalación, con justificación de normativa europea" src="https://github.com/user-attachments/assets/8be2cae2-d728-435f-801f-270cf27333cf" />
        </div>

        <h3>Paso 5. Verificar que la máquina está lista para arrancar</h3>
        <p>
            Antes de comenzar la instalación, se comprueba que la máquina virtual ha quedado correctamente preparada, con su hardware configurado, el disco virtual creado y la ISO asociada al arranque. Esta verificación cierra la fase de preparación y da paso al proceso de instalación del sistema operativo.
        </p>
        <p>
            Las capturas siguientes muestran el inicio del asistente de instalación de Windows 11, confirmando que la máquina arranca correctamente desde la ISO y que el entorno está listo.
        </p>
        <div class="capture-placeholder">
            <img width="747" height="556" alt="Inicio del asistente de instalación de Windows 11 en la máquina virtual" src="https://github.com/user-attachments/assets/8cf26ab2-a500-43d8-bfc2-0808f1837973" />
        </div>
        <div class="capture-placeholder">
            <img width="800" height="580" alt="Progreso de la instalación de Windows 11" src="https://github.com/user-attachments/assets/2f4af1f5-c35a-478c-aaf3-ff5be11be98f" />
        </div>
    </div>

    <div class="content-section">
        <h2 class="sub">Fase 2. Instalación y configuración inicial del sistema</h2>

        <h3>Paso 6. Configurar región, idioma y teclado</h3>
        <p>
            Una vez arranca el asistente de instalación, se selecciona el idioma del sistema, la región y la distribución de teclado. Estas opciones determinan el comportamiento del sistema operativo en cuanto a formatos de fecha, moneda y entrada de texto, por lo que deben ajustarse al entorno de trabajo real.
        </p>
        <div class="capture-placeholder">
            <img width="1056" height="802" alt="Configuración de país e idioma durante la instalación de Windows 11" src="https://github.com/user-attachments/assets/1969b279-d096-4278-8fbc-96c9ec7a4ae2" />
        </div>
        <div class="capture-placeholder">
            <img width="1103" height="802" alt="Configuración de distribución de teclado durante la instalación" src="https://github.com/user-attachments/assets/6efa31f9-c312-475c-909b-fc6d96d070bc" />
        </div>

        <h3>Paso 7. Seleccionar el tipo de uso</h3>
        <p>
            El asistente ofrece distintos perfiles de configuración según el uso previsto del equipo. En este caso se selecciona la opción correspondiente a un entorno personal o de trabajo sin dominio, ya que la máquina virtual opera de forma aislada y no está integrada en ninguna infraestructura de directorio activo.
        </p>
        <div class="capture-placeholder">
            <img width="1096" height="816" alt="Selección del tipo de uso del sistema durante la configuración inicial" src="https://github.com/user-attachments/assets/425ac880-8bdd-437f-9495-1e49f8d6d9ae" />
        </div>

        <h3>Paso 8. Crear usuario y contraseña local</h3>
        <p>
            Se crea una cuenta de usuario local asignándole un nombre de usuario. Opcionalmente puede configurarse una contraseña de acceso; en este caso se ha dejado sin contraseña, lo cual es aceptable en un entorno de máquina virtual aislada destinada a prácticas.
        </p>
        <div class="capture-placeholder">
            <img width="1041" height="788" alt="Pantalla de creación de cuenta de usuario local en Windows 11" src="https://github.com/user-attachments/assets/279d0a6b-fbac-4727-a49c-05588dcd8f6f" />
        </div>
        <div class="capture-placeholder">
            <img width="896" height="481" alt="Introducción del nombre de usuario durante la configuración inicial" src="https://github.com/user-attachments/assets/9cce9aae-a085-4fe6-9194-69eb964c0fc1" />
        </div>
        <div class="capture-placeholder">
            <img width="1096" height="775" alt="Pantalla de contraseña, dejada en blanco para el entorno de prácticas" src="https://github.com/user-attachments/assets/ef799a2d-6cb1-4f17-8e47-8938bedca4bd" />
        </div>

        <h3>Paso 9. Primer inicio de Windows 11</h3>
        <p>
            Una vez completada la configuración inicial, el sistema arranca por primera vez y muestra el escritorio de Windows 11. Este momento confirma que la instalación ha concluido correctamente y que el sistema operativo está operativo dentro de la máquina virtual.
        </p>
        <div class="capture-placeholder">
            <img width="1589" height="913" alt="Primer inicio correcto de Windows 11 en la máquina virtual, escritorio visible" src="https://github.com/user-attachments/assets/71daabba-a7ef-43a9-8622-1bd3e70ed3c0" />
        </div>
    </div>

    <div class="content-section">
        <h2 class="sub">Fase 3. Instalación de VMware Tools y verificación del sistema</h2>

        <h3>Paso 10. Instalar VMware Tools</h3>
        <p>
            Las <strong>VMware Tools</strong> son un conjunto de controladores y utilidades que mejoran significativamente la integración entre el sistema huésped y el hipervisor. Su instalación permite, entre otras funcionalidades, redimensionar la resolución de pantalla automáticamente, habilitar el portapapeles compartido con el equipo anfitrión y mejorar el rendimiento general de la máquina virtual. Sin estas herramientas, la experiencia de uso resulta claramente degradada.
        </p>
        <div class="capture-placeholder">
            <img width="1076" height="777" alt="Inicio de la instalación de VMware Tools desde el menú de VMware" src="https://github.com/user-attachments/assets/bfc7128c-b392-43c9-84a8-7184fe05a4a3" />
        </div>
        <div class="capture-placeholder">
            <img width="607" height="471" alt="Asistente de instalación de VMware Tools en ejecución" src="https://github.com/user-attachments/assets/77cfef29-de20-43ab-8a16-ccd0ed863a95" />
        </div>
        <div class="capture-placeholder">
            <img width="641" height="311" alt="Confirmación de instalación correcta de VMware Tools" src="https://github.com/user-attachments/assets/759d47ff-0a9a-4272-9b03-344478925bb4" />
        </div>

        <h3>Paso 11. Comprobación final del sistema</h3>
        <p>
            Para cerrar la práctica, se verifica que el sistema ha arrancado correctamente, que las VMware Tools están activas y que el entorno general del sistema operativo es estable y funcional. Las capturas siguientes muestran el estado del escritorio y del sistema tras la instalación completa, confirmando que todo ha quedado correctamente configurado.
        </p>
        <div class="capture-placeholder">
            <img width="1564" height="904" alt="Estado final del sistema: escritorio de Windows 11 con VMware Tools instaladas" src="https://github.com/user-attachments/assets/c03c0c68-ca71-4d4c-8412-a949ddd39cb1" />
        </div>
        <div class="capture-placeholder">
            <img width="1600" height="904" alt="Verificación adicional del sistema operativo instalado y en funcionamiento" src="https://github.com/user-attachments/assets/cd9552d8-cc18-4f7c-8e23-888a727e5974" />
        </div>
    </div>
</main>
