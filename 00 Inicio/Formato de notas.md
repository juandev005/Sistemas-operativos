---
tipo: guia
tags: [so/guia]
---
# 📐 Formato para registrar tu aprendizaje

## 1. Dónde se anota cada cosa

| Qué | Dónde | Plantilla |
|---|---|---|
| Aprendizaje de un tema | Sección **Registro por tema** de la nota del módulo | (ya incluida) |
| Un tema que creció mucho | Nota propia (extraída del módulo) | `Plantilla - Tema` |
| Resultado de un laboratorio | Sección **Laboratorios** del módulo; si es largo, nota propia | `Plantilla - Laboratorio` |
| Reto CTF / BTLO / CyberDefenders | Nota propia | `Plantilla - Write-up` |
| Lo que hice hoy | `90 Bitácora/AAAA-MM-DD` | `Plantilla - Bitácora diaria` |
| Comandos y datos de consulta rápida | `91 Cheatsheets/` | libre |

> [!tip] Extraer un tema
> En la nota del módulo, clic derecho sobre el encabezado del tema → **Extract this heading** (plugin core *Note composer*). Luego aplica `Plantilla - Tema`.

## 2. Bloque estándar de un tema

```markdown
### 3. Nombre del tema
- [ ] dominado · dominio: 0 · fecha:
**Mis palabras:** (explícalo como a otra persona, sin copiar)
**Práctica:** (comando, código o lab; usa bloques ```bash)
**Dudas / errores:** (qué falló y por qué)
```

## 3. Escala de dominio (0–5)

| Nivel | Significado |
|---|---|
| 0 | No visto |
| 1 | Lo leí / lo vi |
| 2 | Lo entiendo |
| 3 | Lo explico con mis palabras (Feynman) |
| 4 | Lo practiqué en laboratorio |
| 5 | Lo uso sin ayuda y lo puedo enseñar |

Un tema se marca `dominado` desde el nivel **4**.

## 4. Estados (`estado` en el frontmatter)

`pendiente` → `en-curso` → `dominado` → `repasar`

## 5. Frontmatter de un módulo

```yaml
tipo: modulo
fase: 0
modulo: M0.1
orden: 1          # fase*100 + número, para ordenar bien
horas-estimadas: 8–10
horas-reales: 0
estado: pendiente
```

## 6. Convenciones

- **Enlaza** conceptos relacionados con `[[ ]]`, sobre todo Windows ↔ Linux (ej. auditd ↔ Sysmon, cron ↔ tareas programadas).
- **Etiquetas:** `#so/faseN`, `#so/modulo`, `#so/lab`, `#so/cheatsheet`.
- **Código:** siempre con lenguaje (```bash, ```powershell, ```python).
- **Callouts:** `> [!warning]` errores comunes · `> [!tip]` trucos · `> [!question]` dudas abiertas · `> [!example]` ejemplos.
- **Seguridad:** anota solo laboratorios propios y aislados. Nunca pegues credenciales, tokens ni datos reales.
- **Fuentes:** al final de cada tema, enlace a la documentación oficial usada.

## 7. Tarjetas de repaso

Una por línea, al final del módulo, formato compatible con el plugin *Spaced Repetition*:

```markdown
¿Qué es una syscall?:: Puerta controlada entre modo usuario y modo kernel.
Puerto SMB::445
```

Prioriza datos de alta densidad: event IDs, puertos, comandos, técnicas MITRE, artefactos forenses.

## 8. Ritmo de repaso

- 15–20 min/día de tarjetas.
- Tras cerrar un tema: revisa a los **1, 3, 7, 14 y 30 días**.
- Cada 4–6 semanas, rehaz un laboratorio de una fase anterior.
- Si algo falla en un repaso, cambia `estado` a `repasar`.
