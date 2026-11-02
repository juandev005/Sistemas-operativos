---
tipo: dashboard
tags: [so/dashboard]
---
# 📊 Dashboard

> [!info] Requiere el plugin comunitario **Dataview** (Ajustes → Complementos de la comunidad). Sin él, usa los índices `F0 Índice` … `F7 Índice`.

## Módulos por estado

```dataview
TABLE fase AS Fase, horas-estimadas AS "Horas est.", horas-reales AS "Horas reales", estado AS Estado
FROM #so/modulo
SORT orden ASC
```

## En curso

```dataview
LIST
FROM #so/modulo
WHERE estado = "en-curso"
SORT orden ASC
```

## Para repasar

```dataview
LIST
FROM #so/modulo
WHERE estado = "repasar"
SORT orden ASC
```

## Horas totales dedicadas

```dataview
TABLE sum(rows.horas-reales) AS "Horas reales"
FROM #so/modulo
GROUP BY fase
SORT fase ASC
```

## Bitácora reciente

```dataview
LIST
FROM "90 Bitácora"
SORT file.name DESC
LIMIT 7
```
