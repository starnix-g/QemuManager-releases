# StiexVM

Descargas oficiales de **StiexVM** (antes QemuManager Qt), un gestor de máquinas virtuales QEMU para Windows con interfaz en español.

## Versión terminada: 2.3.0

- Corregido el fallo de arranque que afectaba a equipos con procesadores antiguos. El programa ya no usa instrucciones que esos equipos no entienden.
- Incluye **QEMU 11.0.92**, probado y copiado sin modificar. StiexVM no descarga QEMU de internet ni lo actualiza por su cuenta.
- Si vienes de una versión anterior, el instalador retira los restos viejos antes de copiar los archivos nuevos.
- El equipo no se reinicia sin avisar.

## Todas las arquitecturas, todos los ARM y todos los x86 en prueba: 2.4.3

Es la versión nueva de la línea **2.4.x**. Sigue en el canal de pruebas. Si no quieres probarla, quédate con la versión 2.3.0 de más abajo.

- **Elección en tres niveles.** Primero la arquitectura, después la familia de procesador y por último el modelo concreto. Las listas largas se agrupan en familias cortas (Pentium, Core, Xeon, EPYC, Cortex-A, Cortex-M, Neoverse…). El campo «Otro modelo» sigue permitiendo escribir cualquier nombre de QEMU.
- **Macintosh PowerPC.** Al elegir PowerPC aparece la familia Macintosh, con las placas PowerMac G3 y G4/G5 de QEMU 11.1 y sus procesadores G3, G4 y G5. Sirve para Mac OS clásico y Mac OS X PowerPC (hasta 10.5 Leopard) con una imagen que aportes tú. **QEMU no emula Apple Silicon (M1/M2/M3/M4)** y aquí no se incluye firmware de Apple ni imágenes de macOS.
- **29 arquitecturas en un solo instalador.** Además de x86, están ARM, RISC-V, POWER, MIPS, SPARC, s390x, LoongArch, AVR, Alpha, PA-RISC, SuperH, MicroBlaze, OpenRISC, TriCore, Xtensa, Hexagon y Renesas RX. Se eligen al crear o editar una máquina, en orden histórico.
- **Todos los procesadores x86 de QEMU 11.1.** 188 modelos para x86 de 64 bits y 187 para 32 bits, del 486 de 1990 al Xeon Clearwater Forest de 2025 y el EPYC Turin, pasando por Pentium, Athlon, Core 2, Nehalem, Skylake, Icelake y Sapphire Rapids. Van ordenados por año, con la descripción de QEMU.
- **Todos los procesadores ARM de QEMU 11.1.** ARM de 32 bits ofrece 24 modelos, del StrongARM y ARM9 al Cortex-A15 y Cortex-M55; ARM de 64 bits ofrece 36, del Cortex-A35 al A64FX y Neoverse V1. Hay 93 placas ARM de 32 bits y 108 de 64 bits, desde Integrator y Raspberry Pi hasta las versiones `virt` de QEMU. Los nombres comerciales (Snapdragon, Kirin, Dimensity) no existen en QEMU: se elige el núcleo Cortex en que se basan.
- Hay un campo «Otro modelo» para escribir cualquier otro nombre de CPU de QEMU.
- **Firmware para cada arquitectura** y máquinas antiguas sin cambios: si tu perfil no dice otra cosa, sigue siendo x86 de 64 bits con WHPX.
- Las arquitecturas nuevas se emulan con TCG, porque WHPX solo existe en x86. Algunas aún se están probando con sistemas operativos reales.
- El instalador es más grande: reúne todos los emuladores y su firmware en una sola descarga, sin paquetes aparte.
- Aviso al abrir si hay una versión nueva, siempre con confirmación antes de instalar. Canal beta opcional en **Configuración → Actualizaciones** (viene desactivado).
- Incluye **QEMU 11.1.0** terminado, copiado sin modificar. QEMU nunca se actualiza por separado. StiexVM no reinicia el equipo por su cuenta.

Los números tienen cuatro partes: las tres primeras son la versión y la última cuenta las correcciones. Las versiones de prueba llevan un sufijo. Las correcciones de la línea anterior están en 2.3.1.1, 2.3.1.2 y 2.3.1.3.

## Descargar

### Versión 2.4.3 en el canal de pruebas (opcional)

Instalador: **StiexVM.exe** (versión 2.4.3)

- [Descarga directa](https://github.com/starnix-g/QemuManager-releases/releases/download/beta/StiexVM.exe)
- [Página de la versión beta](https://github.com/starnix-g/QemuManager-releases/releases/tag/beta)
- [Notas de la versión en texto](https://github.com/starnix-g/QemuManager-releases/releases/download/beta/notas-beta.txt)

Tamaño: **164.244.897 bytes**  
SHA256: `fc71f2f8e804dc30c3720a1f805c7eeb29280911c45e3e85f3cf9335b2bc3740`

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
