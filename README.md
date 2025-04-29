# Sistema de Optimización de Rutas con Árbol AVL

**Autor: Ricardo Rincón-2210639**

*---

##  Descripción del Proyecto

Esta segunda versión del sistema de optimización de rutas utiliza un **Árbol AVL** como estructura de datos principal, garantizando balanceo automático tras cada inserción.

Cada ubicación se representa como un nodo con:
- Nombre de la ubicación.
- Conexiones directas a otras ubicaciones.
- Altura para mantener el balance del árbol.

### Funcionalidades principales:
- **Inserción** de ubicaciones en el árbol AVL.
- **Establecimiento de rutas** bidireccionales entre ubicaciones.
- **Búsqueda de rutas** utilizando:
  - **DFS** (Depth First Search).
  - **BFS** (Breadth First Search).
- **Funcionalidad adicionaL: sugerencia de la Ruta Más Cercana** alfabéticamente.

*---

##  Comparativa: Árbol AVL vs Lista Enlazada

| Característica                    | Lista Enlazada Simple      | Árbol AVL                           |------------------------------------|:---------------------------|:------------------------------------|
| Inserción                         | O(1) o O(n)                | O(log n) (balanceo automático)      |
| Búsqueda de ubicación             | O(n)                       | O(log n)                            |
| Búsqueda de rutas (DFS/BFS)       | O(b^d)                     |O(b^d) (acceso más rápido)           |
| Ordenamiento                      |Necesario (BubbleSort O(n²))| Implícito en AVL                    |
| Escalabilidad                     | Limitada                   | Excelente para redes grandes        |
| Complejidad del código            | Baja                       | Moderada (balanceo AVL)             |

**Nota:** El acceso a nodos más eficiente mejora el rendimiento de las búsquedas.

*---

##  Análisis de Complejidad

- **insertar()**: O(log n)
- **buscar()**: O(log n)
- **establecerRuta()**: O(log n)
- **buscarRutaDFS()**: O(b^d)
- **buscarRutaBFS()**: O(b^d)
- **sugerirRutaMasCercana()**: O(1)
- **recorridoInOrder()**: O(n)

**Mejoras respecto a la versión anterior:**
- Eliminación de ordenamientos lentos.
- Mejor acceso a ubicaciones.

*---

##  Nueva Funcionalidad

- **Sugerencia de Ruta Más Cercana:**
  - Si no hay una ruta directa, el sistema sugiere automáticamente el destino más cercano alfabéticamente.
  - Mejora la experiencia del usuario en la navegación entre ubicaciones.

*---

##  Conclusiones

La migración a una estructura AVL logró:
- Reducción significativa de los tiempos de búsqueda e inserción.
- Mayor eficiencia y escalabilidad.
- Eliminación de procesos costosos como el ordenamiento manual.

Este sistema está ahora mejor preparado para aplicaciones de logística, transporte y navegación en redes de mediana a gran escala.

*---

## Estructura del Proyecto

```bash
PROYECTO_V2.py   # Código principal del sistema basado en árbol AVL
README.md        # Documentación técnica (este archivo)
```

