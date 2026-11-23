# QemuManager Qt

Descargas oficiales de **QemuManager Qt**, un gestor de máquinas virtuales QEMU para Windows con interfaz en español.

## Versión terminada: 2.3.0

- Corregido el fallo de arranque que afectaba a equipos con procesadores antiguos. El programa ya no usa instrucciones que esos equipos no entienden.
- Incluye **QEMU 11.0.92**, probado y copiado sin modificar. QemuManager no descarga QEMU de internet ni lo actualiza por su cuenta.
- Si vienes de una versión anterior, el instalador retira los restos viejos antes de copiar los archivos nuevos.
- El equipo no se reinicia sin avisar.

## Corrección en prueba: 2.3.1.1

Es una corrección de errores sobre la 2.3.1-beta3: **no añade funciones**. Sigue en el canal de pruebas hasta que se publique la 2.3.1 terminada. Si no quieres probarla, quédate con la versión 2.3.0 de más abajo.

- **Arreglo de la ayuda.** En las cinco pestañas se puede recorrer el texto con flechas, RePág/AvPág, Inicio/Fin y Ctrl+Inicio/Ctrl+Fin. Antes solo se leía la primera línea. El texto es de solo lectura: se puede copiar, pero no borrar. Lo mismo se aplica al informe de WHPX, al resultado de la comprobación de QEMU, al comando exacto y a las novedades de la actualización.
- Aviso al abrir si hay una versión nueva, siempre con confirmación antes de instalar.
- Canal beta opcional: en **Configuración → Actualizaciones** puedes activar **Recibir versiones beta**. Viene desactivado; si no lo activas, solo se te avisa de las versiones terminadas.
- Más modelos de procesador y de tarjeta de red, más tarjetas gráficas, discos NVMe y teclado y ratón USB.
- Incluye **QEMU 11.1.0** terminado, copiado sin modificar. QEMU nunca se actualiza por separado.
- La descarga muestra una barra de progreso con botón **Cancelar descarga**. Si algo falla al empezar, puedes volver a intentarlo o abrir la página de descarga; no se instala nada a medias.
- Al abrir el programa se retiran los instaladores que hubieran quedado en la carpeta temporal de sesiones anteriores.
- QemuManager sigue sin reiniciar el equipo por su cuenta.

Los números tienen cuatro partes: las tres primeras son la versión y la última cuenta las correcciones, así que 2.3.1.1 es la primera corrección de la 2.3.1. Las versiones de prueba llevan un sufijo, como 2.3.1-beta3. Cuando haya funciones nuevas se pasará a la línea **2.4.x** con sus propias betas.

## Descargar

### Corrección 2.3.1.1 en el canal de pruebas (opcional)

Instalador: **QM.manager.exe** (versión 2.3.1.1)

- [Descarga directa](https://github.com/starnix-g/QemuManager-releases/releases/download/beta/QM.manager.exe)
- [Página de la versión beta](https://github.com/starnix-g/QemuManager-releases/releases/tag/beta)
- [Notas de la versión en texto](https://github.com/starnix-g/QemuManager-releases/releases/download/beta/notas-beta.txt)

Tamaño: **77.861.540 bytes**  
SHA256: `bd03b7f9f72f30ed34bf6399896bfa1a422b7629ceee80332e49ea5864be23e5`

### Versión terminada 2.3.0

Instalador: **QM.manager.exe** (versión 2.3.0)

- [Descarga directa](https://github.com/starnix-g/QemuManager-releases/releases/download/v2.3.0/QM.manager.exe)
- [Página de la versión 2.3.0](https://github.com/starnix-g/QemuManager-releases/releases/tag/v2.3.0)
- [Notas de la versión en texto](https://github.com/starnix-g/QemuManager-releases/releases/download/v2.3.0/notas-v2.3.0.txt)

Tamaño: **65.682.238 bytes**  
SHA256: `8d83c2df3a3685d9ad0989ec50482f7c7abca32bf08bde6b890f6caa22d1ce72`

Los instaladores no están firmados digitalmente. Descárgalos solo desde este sitio. Si quieres comprobar la descarga, abre PowerShell en la carpeta donde lo guardaste y escribe:

```
Get-FileHash "QM.manager.exe" -Algorithm SHA256
```

El valor mostrado debe coincidir con el SHA256 de la versión que descargaste.

## Qué necesitas

- Windows 10 (versión 1809 o posterior) u 11, de 64 bits.
- Virtualización activada en la BIOS o UEFI (Intel VT-x o AMD-V) para que las máquinas vayan a buen ritmo. Sin ella el programa sigue funcionando, pero más lento.
- No necesitas cuenta, correo ni GitHub para descargar o instalar. GitHub solo es el lugar donde se aloja el archivo.

## Sobre este repositorio

Aquí se publican instaladores y notas de versiones. La versión terminada está en la etiqueta `v2.3.0`; la de prueba está en la etiqueta fija `beta` y no sustituye a la terminada. No se publica código fuente.

Si algo no funciona, guarda el mensaje de error o la ruta del registro que muestra el programa y cuéntalo en el lugar donde recibiste el enlace, indicando el modelo del equipo y la versión de Windows.

QemuManager se construyó con la ayuda de **DeepSeek** y otros modelos de lenguaje.
