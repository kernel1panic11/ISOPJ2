<div class="content-section">
    <h2 class="sub">Fase 3. Copias de seguridad y automatización</h2>

    <h3>Paso 12. Creación de un disco para copias</h3>
    <p>
        Se añade un tercer disco virtual destinado exclusivamente a copias de seguridad. Este disco se configura y se formatea en <strong>NTFS</strong>, ya que este sistema de archivos permite trabajar con estructuras de carpetas complejas y mantener integridad en operaciones de copia.
    </p>

    <div class="capture-placeholder">
        <img src="https://github.com/user-attachments/assets/067e00f9-1f5d-404c-8915-7fc4ee026a6f" />
        <img src="https://github.com/user-attachments/assets/422c3d4a-d06b-43b0-9c14-382fd376b93f" />
        <img src="https://github.com/user-attachments/assets/3a2a0cd9-0180-4c17-a194-645138b9db40" />
    </div>

    <h3>Paso 13. Preparación de la estructura de copias</h3>
    <p>
        Dentro del nuevo volumen se crea la carpeta <strong>CopiasUsuaris</strong>, que actuará como directorio raíz para almacenar las copias de los perfiles de usuario.
    </p>

    <div class="capture-placeholder">
        <img src="https://github.com/user-attachments/assets/4b137df3-2df8-4546-84ed-8f9d00105316" />
    </div>

    <h3>Paso 14. Creación del script de copia</h3>
    <p>
        Se crea un script en formato <code>.bat</code> que copia el contenido de la carpeta del usuario activo (<code>C:\Users\%USERNAME%</code>) a su correspondiente carpeta dentro de <code>E:\CopiasUsuaris</code>. Esto permite automatizar una copia básica del perfil de usuario.
    </p>

    <div class="capture-placeholder">
        <img src="https://github.com/user-attachments/assets/cf16bda6-e283-4181-bc25-bdfb48d40b43" />
    </div>

    <h3>Paso 15. Automatización con gpedit</h3>
    <p>
        El script se configura para ejecutarse automáticamente al iniciar sesión mediante el editor de directivas locales (<code>gpedit.msc</code>). De este modo, cada usuario genera su copia de forma automática al acceder al sistema.
    </p>

    <div class="capture-placeholder">
        <img src="https://github.com/user-attachments/assets/ca9e2b85-78a1-4721-abfe-b147550a68a4" />
        <img src="https://github.com/user-attachments/assets/7ff2c20b-02a6-4591-90e2-6254579a72b5" />
        <img src="https://github.com/user-attachments/assets/106b705e-2a62-4b23-9c5e-51f91558df11" />
    </div>
</div>

<div class="content-section">
    <h2 class="sub">Fase 4. Verificación de copias</h2>

    <h3>Paso 16. Prueba con usuario</h3>
    <p>
        Se inicia sesión con el usuario <strong>alumne1</strong> para comprobar que el script se ejecuta correctamente en el arranque de sesión.
    </p>

    <div class="capture-placeholder">
        <img src="https://github.com/user-attachments/assets/f32b8a56-d056-4385-9627-91348b073f49" />
    </div>

    <h3>Paso 17. Comprobación de resultados</h3>
    <p>
        Se verifica que la carpeta correspondiente al usuario se ha creado dentro de <strong>CopiasUsuaris</strong> y contiene los datos copiados. Esto confirma que la automatización funciona correctamente.
    </p>

    <div class="capture-placeholder">
        <img src="https://github.com/user-attachments/assets/fe681ef2-d701-41b9-83d0-80e034c2d428" />
    </div>
</div>

<div class="content-section">
    <h2 class="sub">Fase 5. Gestión de procesos</h2>

    <h3>Paso 18. Listado de procesos</h3>
    <p>
        Se utiliza el comando <code>tasklist</code> para obtener un listado completo de los procesos en ejecución en el sistema.
    </p>

    <div class="capture-placeholder">
        <img src="https://github.com/user-attachments/assets/0eced897-a4aa-4066-a81d-786f5629188c" />
    </div>

    <h3>Paso 19. Guardado de evidencia</h3>
    <p>
        La salida del comando se guarda en un archivo para su posterior análisis y documentación, permitiendo revisar los procesos activos fuera del entorno de ejecución.
    </p>

    <div class="capture-placeholder">
        <img src="https://github.com/user-attachments/assets/56c67097-9d32-4590-8f52-b68be2122a5b" />
        <img src="https://github.com/user-attachments/assets/b70dee83-99dc-4e68-aa07-deccef6e5eea" />
    </div>

    <h3>Paso 20. Identificación de procesos prescindibles</h3>
    <p>
        A partir del listado, se identifican procesos no esenciales que pueden eliminarse para optimizar el rendimiento del sistema en un entorno virtual.
    </p>

    <table>
        <tr><th>Proceso</th><th>Memoria usada</th><th>Justificación</th></tr>
        <tr><td>OneDrive.exe</td><td>139.180 KB</td><td>Sin sincronización activa en VM.</td></tr>
        <tr><td>msedgewebview2.exe</td><td>~125.000 KB</td><td>Motor de widgets no esencial.</td></tr>
        <tr><td>WidgetBoard.exe</td><td>105.664 KB</td><td>Widgets innecesarios.</td></tr>
        <tr><td>SearchHost.exe</td><td>129.488 KB</td><td>Indexado prescindible.</td></tr>
        <tr><td>RuntimeBroker.exe</td><td>~60.000 KB</td><td>Consumo acumulado.</td></tr>
    </table>

    <h3>Paso 21. Finalización de procesos</h3>
    <p>
        Se eliminan procesos no esenciales mediante <code>taskkill</code>, liberando recursos del sistema.
    </p>

    <div class="capture-placeholder">
        <img src="https://github.com/user-attachments/assets/cea0577b-eadf-4b3f-a8da-8baa509325e2" />
        <img src="https://github.com/user-attachments/assets/ba01c5d7-f976-474f-b76e-f460a68da850" />
        <img src="https://github.com/user-attachments/assets/2392018d-01cb-412e-9154-5ff071d0e1dc" />
    </div>

    <h3>Paso 22. Verificación con otro usuario</h3>
    <p>
        Se inicia sesión con <strong>alumne2</strong> para comprobar que los procesos eliminados no se ejecutan automáticamente, verificando así la persistencia de la optimización realizada.
    </p>

    <div class="capture-placeholder">
        <img src="https://github.com/user-attachments/assets/57a29a74-961f-4755-85e6-ef147c86db17" />
        <img src="https://github.com/user-attachments/assets/a7cdfcde-8583-481a-8993-f24697742474" />
    </div>

    <p>
        Esta gestión permite reducir el consumo de recursos en máquinas virtuales, mejorando la eficiencia del sistema y evitando la ejecución de servicios innecesarios.
    </p>
</div>
