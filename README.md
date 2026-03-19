# Dell Inspiron 3250 Hackintosh - macOS Monterey (OpenCore)

Este repositorio contiene la carpeta EFI optimizada para ejecutar macOS Monterey de forma estable en una Dell Inspiron 3250. Diseñado para entornos de desarrollo de software (SQL, Flask) y producción musical (GarageBand/iPod Management).

## ⚡ Especificaciones Técnicas
* **CPU:** Intel Core i5-6400 (Skylake) @ 2.70GHz
* **GPU:** Intel HD Graphics 530 (Aceleración Metal Nativa - 1536 MB VRAM)
* **RAM:** 12 GB DDR3L/DDR4 (Configuración probada)
* **Audio:** Realtek ALC (Layout ID: 13)
* **Ethernet:** Realtek RTL8111
* **Bootloader:** OpenCore

## ✅ ¿Qué funciona?
* Aceleración gráfica completa (QE/CI) con soporte Metal.
* Audio integrado (Entrada/Salida y Jack frontal).
* Gestión de energía y reposo (Sleep/Wake) corregido.
* Todos los puertos USB (3.0 y 2.0).
* Servicios de Apple (App Store, Music, iCloud).
* Sincronización nativa de iPods vía iTunes/Music.

## 🛠️ Instrucciones de Instalación
He trabajado esta EFI suponiendo que el usuario no tiene conocimientos profundos de programación. Siga estos pasos:

1. **Descarga:** Clone este repositorio o descargue la carpeta EFI.
2. **Seguridad:** El archivo `config.plist` incluido es un **Template**. DEBE generar sus propios números de serie (MLB, ROM, SystemSerialNumber, SystemUUID) usando herramientas como `GenSMBIOS`.
3. **BIOS:** Asegúrese de tener desactivado el *Secure Boot* y configurado el SATA en modo *AHCI*.
4. **Post-Instalación:** Si el audio no se detecta, verifique que el `boot-arg` mantenga `alcid=13`.

## ⚠️ Nota de Seguridad
Por razones de seguridad y para evitar el bloqueo de cuentas de Apple, los valores de `PlatformInfo` se han dejado en blanco. No intente arrancar sin antes generar sus propios seriales.
