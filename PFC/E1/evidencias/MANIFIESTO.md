# Manifiesto de evidencias privadas — TA-PFC-E1

Los originales de estas evidencias **no se publican** en este repositorio porque contienen
datos personales de terceros (LOPDP). Se custodian en la carpeta institucional privada del
equipo (cuenta `@uteq.edu.ec`), compartida con el docente.

- **Carpeta privada:** _(nombre de la carpeta, no el enlace público)_
- **Administrador de la carpeta:** _(rol / integrante del equipo)_

La huella SHA-256 permite comprobar que el archivo original no fue modificado. Se calcula con:

```powershell
# Windows (PowerShell)
Get-FileHash -Algorithm SHA256 .\archivo.pdf
```

```bash
# Linux / macOS / Git Bash
sha256sum archivo.pdf
```

| ID | Archivo (en la carpeta privada) | Tipo | Fecha | Duración | SHA-256 |
|----|---------------------------------|------|-------|----------|---------|
| EV-01 | `EV01_carta_aceptacion.pdf` | Carta de aceptación firmada | AAAA-MM-DD | — | _(64 caracteres hex)_ |
| EV-02 | `EV02_registro_primer_contacto.pdf` | Registro / acta del primer contacto | AAAA-MM-DD | _(min)_ | _(64 caracteres hex)_ |

> Agregue una fila por cada consentimiento firmado, audio o fotografía que se genere en las
> sesiones (EV-03, EV-04, ...). Use códigos (P01, P02) en los nombres de archivo, nunca nombres
> de personas.
