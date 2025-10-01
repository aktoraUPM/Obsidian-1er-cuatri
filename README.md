# Apuntes de Ingeniería Electrónica Industrial y Automática UPM.
### Descripción
Estos son mis apuntes del primer cuatrimestre de Ingeniería Electrónica Industrial y Automática en la Universidad Politécnica de Madrid.
### Editor: Obsidian
Los apuntes están hechos en **[Obsidian](https://obsidian.md/)**, y si bien es posible exportarlos a PDF o abrirlos en cualquier visor de MarkDown (salvo los gráficos de TikZ y/o que no tenga renderizado de LaTeX), lo mejor es visualizarlos utilizando esta misma aplicación, pues utilizo plugins de esta para editarlos, además de que incluye alguna gráfica en TikZ que no se puede ver a través de MarkDown común.
##### Instalación de Obsidian
- A través del instalador normal, que se puede obtener [aquí](https://obsidian.md/download).
- **(Opción más rápida)** A través del instalador `winget` del CMD. Buscando *cmd* en las aplicaciones de Windows, se abre una ventana de terminal. Ahí, si se tiene instalado, basta con ejecutar 
  ```
  winget install Obsidian.Obsidian
  ```
  Y aceptar la descarga cuando lo pida (escribiendo `Y + Enter`, no sé si en Windows es suficiente con sencillamente `Enter` como en APT).
### Uso de los apuntes
##### Propiedad
- Son mis apuntes, pero me importa poco donde acaben, si no, no los subía a GitHub. Úsense con total libertad.
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
##### Dependencias en Obsidian
- [**TikZJax**](obsidian://show-plugin?id=obsidian-tikzjax). Sin este plugin de Obsidian, los gráficos en TikZ no se renderizan, es necesario instalarlo en *Options > Community plugins > Browse > TikZJax > Install + Enable*. Si no se habilita, sólo aparecerán bloques largos y feos de cógigo encabezados por un `tikz`.
- El repositorio incluye mis macros personalizados para [**Latex Suite**](obsidian://show-plugin?id=obsidian-latex-suite) (plugin de macros para LaTeX), si se quiere editar los apuntes es recomendable considerar si se quieren eliminar o no.