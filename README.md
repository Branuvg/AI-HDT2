# CC3045 - Inteligencia Artificial
## Hoja de Trabajo 2 - Frozen Lake MDP

Implementación de un Proceso de Decisión de Markov (MDP) para el entorno "Frozen Lake" utilizando el algoritmo de Value Iteration.

---

## Descripción

El proyecto implementa desde cero un agente que navega un lago congelado de 4x4 con hielo resbaladizo, llegando desde el inicio (S) hasta la meta (G) evitando agujeros (H).

---

## Estructura

```
AI-HDT2/
├── README.md                
└── task2.ipynb              # Notebook con la implementación completa
```

---

## Implementación

### Task 2.1 - Modelado del MDP
Clase `FrozenLakeMDP` con:
- **Estados**: 16 estados (0-15) en cuadrícula 4x4
- **Acciones**: 4 direcciones (Norte=0, Sur=1, Este=2, Oeste=3)
- **Transición T(s,a,s')**: P=1/3 dirección deseada, P=1/3 cada perpendicular
- **Recompensa R(s,a,s')**: +1 solo al alcanzar meta (G)

### Task 2.2 - Value Iteration
Algoritmo completo con:
1. Inicialización: V₀(s) = 0
2. Iteración hasta convergencia (ε = 1e-6)
3. Extracción de política π*(s)
4. Visualización de resultados

---

## Requisitos

```python
import numpy as np
import matplotlib.pyplot as plt
import matplotlib.colors as mcolors
```

**Restricciones**: Solo numpy, pandas, matplotlib. PROHIBIDO sklearn, pytorch, tensorflow.

---

## Ejecución

```bash
jupyter notebook task2.ipynb
```

Ejecutar las celdas en orden:
1. Definición de `FrozenLakeMDP`
2. Instanciación del MDP
3. Value Iteration
4. Visualización

---

## Ecuaciones

**Bellman**:
```
V_{k+1}(s) = max_a Σ_{s'} T(s,a,s') · [R(s,a,s') + γ · V_k(s')]
```

**Política**:
```
π*(s) = argmax_a Σ_{s'} T(s,a,s') · [R(s,a,s') + γ · V*(s')]
```

---

## Integrantes

* Gabriel Bran - 23590 
* David Dominguez - 23712


---

**CC3045 - Inteligencia Artificial - I Semestre 2026**