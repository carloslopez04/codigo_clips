## Ejercicio de Código_Clips 

 * Borja Bravo Casermeiro
 * Carlos López Muñoz

# Sistema Difuso para el Control de Temperatura del Horno

## Descripción del Proyecto

La Abuela María ha perfeccionado la receta de sus deliciosas galletas caseras durante más de 40 años, utilizando un proceso artesanal que depende de ajustar la temperatura del horno según el estado de las galletas. Este repositorio implementa un sistema automatizado basado en lógica difusa para replicar este proceso y garantizar el característico color dorado de las galletas.

### Reglas del Sistema
El sistema utiliza un índice cromático especial para determinar el estado de las galletas (0 = cruda, 10 = chamuscada) y ajusta la temperatura del horno siguiendo las siguientes reglas:

1. **Un poco crudas**: Si las galletas están un poco crudas, la temperatura debe ser **media**.
2. **Medio hechas**: Si las galletas están medio hechas, la temperatura debe ser **alta**.
3. **Doraditas**: Si las galletas están doraditas, la temperatura debe ser **baja**.

### Conjuntos Difusos

#### Índice Cromático de las Galletas:
- **Un poco crudas**: (1/4, 0.5/6, 0/7)
- **Medio hechas**: (0/3, 1/5, 1/6, 0/8)
- **Doraditas**: (0/5, 1/7)

#### Temperatura del Horno (°C):
- **Baja**: (0/150, 1/160, 1/180, 0/190)
- **Media**: (0/170, 1/190, 1/210, 0/230)
- **Alta**: (0/210, 1/220, 1/240, 0/250)

### Ejemplo
En este proyecto, se implementa un sistema en **CLIPS** para calcular automáticamente la temperatura ideal del horno dado un índice cromático de las galletas. Por ejemplo, si el índice cromático es 6, el sistema aplicará las reglas difusas para determinar la temperatura adecuada.

---

## Requisitos

- **Lenguaje**: CLIPS
- **Software**: [CLIPS](https://www.clipsrules.net/)
- Trabajo realizado por parejas.

---

## Estructura del Proyecto

- `base_de_conocimientos.clp`: Contiene las reglas del sistema basadas en los conjuntos difusos.
- `base_de_hechos.clp`: Incluye los hechos iniciales del sistema, como el índice cromático actual de las galletas.
- `README.md`: Documentación del proyecto (este archivo).

