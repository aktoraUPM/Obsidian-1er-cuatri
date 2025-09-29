# Apuntes de Ingeniería Electrónica Industrial y Automática UPM.
### Descripción
Estos son mis apuntes del primer cuatrimestre de Ingeniería Electrónica Industrial y Automática en la Universidad Politécnica de Madrid.
### Editor: Obsidian
Los apuntes están hechos en **Obsidian**, y si bien es posible exportarlos a PDF o abrirlos en cualquier visor de MarkDown, lo mejor es visualizarlos utilizando esta misma aplicación, pues utilizo plugins de esta para editarlos, además de que incluye alguna gráfica en TikZ que no se puede ver a través de MarkDown común.
##### Instalación de Obsidian
- A través del instalador normal, que se puede obtener [aquí](https://obsidian.md/download).
- **(Opción más rápida)** A través del instalador `winget` del CMD. Buscando *cmd* en las aplicaciones de Windows, se abre una ventana de terminal. Ahí, si se tiene instalado, basta con ejecutar 
  ```
  winget install Obsidian.Obsidian
  ```
  Y aceptar la descarga cuando lo pida (escribiendo `Y + Enter`, no sé si en Windows es suficiente con sencillamente `Enter` como en APT).
### Los propios apuntes
##### Descarga
- A través de esta misma página de GitHub, en el [enlace de descarga del botón verde](https://github.com/aktoraUPM/Obsidian-1er-cuatri/archive/refs/heads/master.zip).
- Con **Git**, para quien no sepa qué es, viene instalado en Mac y Linux, en Windows se puede instalar también fácilmente con winget a través de
  ```
  winget install Git.Git
  ```
  Una vez instalado, basta con escribir en terminal
  ```
  git clone https://github.com/aktoraUPM/Obsidian-1er-cuatri.git
  ```
##### Abrir los apuntes
Al abrirlos en Obsidian, solicitará activar los plugins. Son todos descargados de la página de **Community plugins** de Obsidian, son perfectamente seguros, por lo que basta con darle a _Trust the author_ al importar esta vault.
Es necesario utilizar al menos `TikZJaz`, hay gráficos que se tienen que renderizar con TikZ y si no solo serán bloques largos y feos de código encabezados por un `tikz`.
Los macros para $\LaTeX$ del plugin *LaTeX Suite* están personalizados, pero creo que no son malas elecciones. Tampoco están optimizados ni nada por el estilo, son los que se me iban ocurriendo cuando los necesitaba.