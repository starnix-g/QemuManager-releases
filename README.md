# StiexVM

Descargas oficiales de **StiexVM** (antes QemuManager Qt), un gestor de máquinas virtuales QEMU para Windows con interfaz en español.

## Versión terminada: 2.3.0

- Corregido el fallo de arranque que afectaba a equipos con procesadores antiguos. El programa ya no usa instrucciones que esos equipos no entienden.
- Incluye **QEMU 11.0.92**, probado y copiado sin modificar. StiexVM no descarga QEMU de internet ni lo actualiza por su cuenta.
- Si vienes de una versión anterior, el instalador retira los restos viejos antes de copiar los archivos nuevos.
- El equipo no se reinicia sin avisar.

GitHub marca **v2.3.0** como *Latest* porque la beta es una versión preliminar. La última beta está en la etiqueta fija `beta` y se describe abajo.

## Canal de pruebas: 2.5.7

Esta línea sigue en el canal de pruebas. La versión terminada sigue siendo la 2.3.0.

### 2.5.7 — arranque directo, actualizaciones visibles y lista de máquinas

Corrección de la 2.5.6, sin funciones nuevas.

- La máquina arranca directamente: con disco e ISO se intenta primero el disco y la ISO queda como respaldo. Ya no aparece el «Press any key to boot from CD...».
- Se quitó el menú de arranque: QEMU no recibe `menu=on` y la opción desapareció de «Editar».
- El actualizador vuelve a avisar: acepta los servidores de objetos de GitHub, siempre por HTTPS, con tamaño y SHA256 verificados. Las betas solo se ofrecen si «Recibir versiones beta» está activado.
- Las máquinas están en una lista, con nombre y estado en cada fila. Supr elimina la elegida y Enter abre la seleccionada y activa casillas y opciones.

### 2.5.6 — recursos razonables, captura inmediata y sin consolas

- El creador propone un cuarto de la RAM, en bloques de 4 GB y entre 2 y 16 GB.
- Ctrl+Alt+Enter captura el teclado aunque la máquina no esté cargada.
- No se abren consolas de QEMU al actualizar ni al iniciar.

### Histórico de la línea 2.4

**2.4.6.1 — corrección de errores.** Audio con búferes cortos encadenados, visor sin barras visibles, avisos de captura y menús completos del cliente pequeño.

**2.4.6 — pantalla SPICE y control de la máquina.** Visor SPICE integrado, teclado con scancodes reales, menús con reiniciar, apagar, suspender, continuar y detener, y configuración por pestañas.

**2.4.5 — pantalla integrada y audio estable.** Pantalla dentro de StiexVM desde el inicio, teclado capturado que llega a la máquina, puertos libres automáticos y audio sin cortes.

**2.4.4 — detención de máquinas.** Aviso claro de detención inmediata, estado «Deteniéndose» y salida forzada si el proceso sigue vivo.

**2.4.3 — elección por familia y Macintosh PowerPC.** Arquitectura, familia y modelo, con Macs G3/G4/G5 y firmware por arquitectura.

**2.4.2 y 2.4.1 — listas completas.** 29 arquitecturas, todos los procesadores x86 y ARM de QEMU 11.1 y campo «Otro modelo».

Los números tienen cuatro partes: las tres primeras son la versión y la última cuenta las correcciones. Las versiones de prueba llevan un sufijo. Las correcciones de la línea anterior están en 2.3.1.1, 2.3.1.2 y 2.3.1.3.

## Descargar

### Versión 2.5.7 en el canal de pruebas (opcional)

Instalador: **StiexVM.exe** (versión 2.5.7), con QEMU 11.1.0 incluido y sin modificar.

- [Descarga directa](https://github.com/starnix-g/StiexVM-releases/releases/download/beta/StiexVM.exe)
- [Página de la versión beta](https://github.com/starnix-g/StiexVM-releases/releases/tag/beta)
- [Notas de la versión en texto](https://github.com/starnix-g/StiexVM-releases/releases/download/beta/notas-beta.txt)
- [Manifiesto que lee el actualizador](https://github.com/starnix-g/StiexVM-releases/releases/download/beta/latest.json)

Enlace permanente de la beta: https://github.com/starnix-g/StiexVM-releases/releases/tag/beta

Tamaño: **215.543.505 bytes**  
SHA256: `b392808984e255045dd3e39aeddbc07993dcaa375854b0534c44a152fdc215ee`

### Versión terminada 2.3.0

Instalador: **QM.manager.exe** (versión 2.3.0)

- [Descarga directa](https://github.com/starnix-g/StiexVM-releases/releases/download/v2.3.0/QM.manager.exe)
- [Página de la versión 2.3.0](https://github.com/starnix-g/StiexVM-releases/releases/tag/v2.3.0)
- [Notas de la versión en texto](https://github.com/starnix-g/StiexVM-releases/releases/download/v2.3.0/notas-v2.3.0.txt)

Tamaño: **65.682.238 bytes**  
SHA256: `8d83c2df3a3685d9ad0989ec50482f7c7abca32bf08bde6b890f6caa22d1ce72`

Los instaladores no están firmados digitalmente. Descárgalos solo desde este sitio. Si quieres comprobar la descarga, abre PowerShell en la carpeta donde lo guardaste y escribe:

```
Get-FileHash "StiexVM.exe" -Algorithm SHA256
```

El valor mostrado debe coincidir con el SHA256 de la versión que descargaste.

## Qué necesitas

- Windows 10 (versión 1809 o posterior) u 11, de 64 bits.
- Virtualización activada en la BIOS o UEFI (Intel VT-x o AMD-V) para que las máquinas vayan a buen ritmo. Sin ella el programa sigue funcionando, pero más lento.
- No necesitas cuenta, correo ni GitHub para descargar o instalar. GitHub solo es el lugar donde se aloja el archivo.

## Sobre este repositorio

Aquí se publican instaladores y notas de versiones. La versión terminada está en la etiqueta `v2.3.0`; la de prueba está en la etiqueta fija `beta` y no sustituye a la terminada. No se publica código fuente.

Si algo no funciona, guarda el mensaje de error o la ruta del registro que muestra el programa y cuéntalo en el lugar donde recibiste el enlace, indicando el modelo del equipo y la versión de Windows.

StiexVM se construyó con la ayuda de **DeepSeek** y otros modelos de lenguaje.
