# 🧩 Challenges y Coding Tests (2025)

> Estrategia para entregar pruebas técnicas con calidad y en tiempo.

## Enfoque de entrega
1) Aclara requerimientos y criterios (alcance, I/O, edge cases)
2) Diseña antes de codear (pequeño README + diagrama simple)
3) Itera en vertical: MVP → features → polish
4) Testing mínimo y script de ejecución "1-click"

## Estructura recomendada
```
proyecto/
├── README.md (setup, scripts, decisiones)
├── src/
├── tests/
└── scripts/ (seed, lint, verify)
```

## README del challenge (plantilla)
```markdown
# Solución – [Challenge]

## Setup
- Requisitos, scripts, variables

## Decisiones
- Arquitectura, trade-offs, complejidad

## Tests
- Qué se cubre y cómo correrlos

## Futuro
- Mejoras y extensiones
```

## Entregables que destacan
- Instrucciones claras y reproducibles
- Pruebas y casos edge representativos
- Manejo de errores y límites
- Observabilidad mínima (logs/metrics en backend)

## Evita
- Commits enormes sin contexto
- Falta de README o scripts
- Ignorar performance y seguridad básicas

---

Actualizado: Octubre 2025
