# StiexVM

Descargas oficiales de **StiexVM** (antes QemuManager Qt), un gestor de máquinas virtuales QEMU para Windows con interfaz en español.

## Versión terminada: 2.3.0

- Corregido el fallo de arranque que afectaba a equipos con procesadores antiguos. El programa ya no usa instrucciones que esos equipos no entienden.
- Incluye **QEMU 11.0.92**, probado y copiado sin modificar. StiexVM no descarga QEMU de internet ni lo actualiza por su cuenta.
- Si vienes de una versión anterior, el instalador retira los restos viejos antes de copiar los archivos nuevos.
- El equipo no se reinicia sin avisar.

## Cambio de nombre en prueba: 2.3.1.2

Es un ajuste sobre la 2.3.1.1: **no añade funciones** y sigue en el canal de pruebas. El programa pasa a llamarse **StiexVM**. Si no quieres probarlo, quédate con la versión 2.3.0 de más abajo.

- El nombre nuevo aparece en la ventana, la ayuda y los mensajes. El archivo que se descarga es `StiexVM.exe`.
- Tus máquinas siguen donde estaban: la carpeta de perfiles, la carpeta de instalación y el actualizador no cambian de sitio. No hay que mover ni volver a crear nada.
- Al actualizar se retiran el ejecutable y los accesos directos del nombre anterior, para que no queden dos entradas en el menú.
- Aviso al abrir si hay una versión nueva, siempre con confirmación antes de instalar.
- Canal beta opcional: en **Configuración → Actualizaciones** puedes activar **Recibir versiones beta**. Viene desactivado; si no lo activas, solo se te avisa de las versiones terminadas.
- Incluye **QEMU 11.1.0** terminado, copiado sin modificar. QEMU nunca se actualiza por separado.
- La descarga muestra una barra de progreso con botón **Cancelar descarga**. Si algo falla al empezar, puedes volver a intentarlo o abrir la página de descarga; no se instala nada a medias.
- StiexVM no reinicia el equipo por su cuenta.

Los números tienen cuatro partes: las tres primeras son la versión y la última cuenta las correcciones, así que 2.3.1.2 es la segunda corrección de la 2.3.1. Las versiones de prueba llevan un sufijo, como 2.3.1-beta3. Cuando haya funciones nuevas se pasará a la línea **2.4.x** con sus propias betas.

## Descargar

### Versión 2.3.1.2 en el canal de pruebas (opcional)

Instalador: **StiexVM.exe** (versión 2.3.1.2)

- [Descarga directa](https://github.com/starnix-g/QemuManager-releases/releases/download/beta/StiexVM.exe)
- [Página de la versión beta](https://github.com/starnix-g/QemuManager-releases/releases/tag/beta)
- [Notas de la versión en texto](https://github.com/starnix-g/QemuManager-releases/releases/download/beta/notas-beta.txt)

Tamaño: **77.873.371 bytes**  
SHA256: `d31a6519faaccb2748a8508ad66aa7d4087afc1cf237ea9322564c3561d5123b`

### Versión terminada 2.3.0

Instalador: **QM.manager.exe** (versión 2.3.0)

- [Descarga directa](https://github.com/starnix-g/QemuManager-releases/releases/download/v2.3.0/QM.manager.exe)
- [Página de la versión 2.3.0](https://github.com/starnix-g/QemuManager-releases/releases/tag/v2.3.0)
- [Notas de la versión en texto](https://github.com/starnix-g/QemuManager-releases/releases/download/v2.3.0/notas-v2.3.0.txt)

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
