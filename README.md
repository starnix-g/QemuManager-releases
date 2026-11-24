# StiexVM

Descargas oficiales de **StiexVM** (antes QemuManager Qt), un gestor de máquinas virtuales QEMU para Windows con interfaz en español.

## Versión terminada: 2.3.0

- Corregido el fallo de arranque que afectaba a equipos con procesadores antiguos. El programa ya no usa instrucciones que esos equipos no entienden.
- Incluye **QEMU 11.0.92**, probado y copiado sin modificar. StiexVM no descarga QEMU de internet ni lo actualiza por su cuenta.
- Si vienes de una versión anterior, el instalador retira los restos viejos antes de copiar los archivos nuevos.
- El equipo no se reinicia sin avisar.

## Cambios recientes de la línea 2.4

Esta línea sigue en el canal de pruebas. La versión terminada es la 2.3.0, más abajo.

### 2.4.4 — detención de máquinas

- El diálogo de detención indica que la máquina se detiene de forma inmediata y que los cambios pendientes del sistema invitado podrían no guardarse. Se retiraron comparaciones y ejemplos innecesarios.
- El botón pasa a «Deteniendo…» y queda desactivado en cuanto se confirma la detención, sin esperar al sondeo del proceso. La lista muestra «Deteniéndose» y, al terminar el proceso, el botón vuelve a «Iniciar».
- Si el proceso sigue activo tres segundos después de pedir la detención, se fuerza su salida.
- Una detención manual cancela cualquier reinicio automático registrado por un aviso anterior de la máquina.

### 2.4.3 — elección por familia y Macintosh PowerPC

- Arquitectura, familia de procesador y modelo concreto, en ese orden. Las listas largas se agrupan en bloques cortos (Pentium, Core, Xeon, EPYC, Cortex-A, Cortex-M, Neoverse…), con un orden fijo que permite recorrerlas con Tab.
- Macintosh PowerPC: placas PowerMac G3 y G4/G5 de QEMU 11.1, con procesadores G3, G4 y G5. Permite Mac OS clásico y Mac OS X PowerPC hasta 10.5 Leopard con una imagen de sistema aportada por el usuario.
- Apple Silicon: no está entre las máquinas del QEMU 11.1 distribuido. La nota de la arquitectura lo indica en la interfaz.

### 2.4.2 y 2.4.1 — listas completas

- 29 arquitecturas en un solo instalador: ARM, RISC-V, POWER, MIPS, SPARC, s390x, LoongArch, AVR, Alpha, PA-RISC, SuperH, MicroBlaze, OpenRISC, TriCore, Xtensa, Hexagon y Renesas RX, además de x86. Se eligen al crear o editar una máquina, en orden histórico.
- Todos los procesadores x86 de QEMU 11.1: 188 modelos para x86 de 64 bits y 187 para 32 bits, del 486 de 1990 al Xeon Clearwater Forest de 2025 y el EPYC Turin, ordenados por año y con la descripción de QEMU.
- Todos los procesadores ARM de QEMU 11.1: 24 modelos de 32 bits y 36 de 64 bits, con 93 y 108 placas respectivamente. Los nombres comerciales (Snapdragon, Kirin, Dimensity) no existen en QEMU: se elige el núcleo Cortex en que se basan.
- El campo «Otro modelo» admite cualquier otro nombre de CPU de QEMU.
- Firmware para cada arquitectura. Los perfiles existentes siguen con x86 de 64 bits y WHPX salvo indicación contraria.
- Las arquitecturas nuevas se emulan con TCG, porque WHPX solo existe en x86. Algunas aún se están probando con sistemas operativos reales.
- Aviso al abrir si hay una versión nueva, siempre con confirmación. Canal beta opcional en Configuración → Actualizaciones, desactivado por defecto.
- Incluye QEMU 11.1.0 copiado sin modificar. QEMU nunca se actualiza por separado y el equipo no se reinicia sin aviso.

Los números tienen cuatro partes: las tres primeras son la versión y la última cuenta las correcciones. Las versiones de prueba llevan un sufijo. Las correcciones de la línea anterior están en 2.3.1.1, 2.3.1.2 y 2.3.1.3.

## Descargar

### Versión 2.4.4 en el canal de pruebas (opcional)

Instalador: StiexVM.exe (versión 2.4.4)

- [Descarga directa](https://github.com/starnix-g/QemuManager-releases/releases/download/beta/StiexVM.exe)
- [Página de la versión beta](https://github.com/starnix-g/QemuManager-releases/releases/tag/beta)
- [Notas de la versión en texto](https://github.com/starnix-g/QemuManager-releases/releases/download/beta/notas-beta.txt)

Tamaño: 164.241.855 bytes  
SHA256: `ff20ce5c602d2847005e8bc114f657746828086870e3f0f96141b3f8f50df225`

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
