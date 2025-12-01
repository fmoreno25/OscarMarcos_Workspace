
# Contexto del Proyecto – Q65 y Reprogramación de Tapajuntas / Solapes

## 1. Objetivo General

Reunir toda la información técnica necesaria para:

* Programar correctamente la serie **Q65**.
* Integrar la lógica de **tapajuntas** y **solapes**.
* Controlar reglas y mecanizados relacionados con **persianas**, **guías**, **incompatibilidades** y **mecanizados automáticos**.
* Preparar todos los insumos para generar las tareas precisas y luego desarrollar los scripts.

---

## 2. Opciones / Decisiones de Configuración

### 2.1 Taladros de Instalación (Obra)

| Ubicación                                           | Opción                                                    | Tipo     | Valores | Disparadas                               |
| --------------------------------------------------- | --------------------------------------------------------- | -------- | ------- | ---------------------------------------- |
| Nivel1 = Instalación Obra                           | Taladro Marco                                             | Decisión | Sí/No   | —                                        |
| Nivel1 = Instalación Obra / Nivel2 = Tramos Taladro | Tal_Derecha / Tal_Inferior / Tal_Izquierda / Tal_Superior | Decisión | Sí/No   | Si va con persiana → tramo superior = No |

### 2.2 Cinta Transporte

| Ubicación        | Opción | Tipo     | Valores |
| ---------------- | ------ | -------- | ------- |
| Cinta Transporte | —      | Decisión | Sí/No   |

---

## 3. Mecanizados

### 3.1 Instalación Obra

| Mecanizado   | Tipo         | Ubicación                                   | Incompatibilidades                        |
| ------------ | ------------ | ------------------------------------------- | ----------------------------------------- |
| Taladro Obra | Círculo 5 mm | Exterior marco – 2 taladros + 1 cada 300 mm | Desplazar cuando va Recogedor de Persiana |

### 3.2 Cinta Transporte

| Mecanizado               | Tipo         | Ubicación                                     |
| ------------------------ | ------------ | --------------------------------------------- |
| Taladro Cinta Transporte | Círculo 3 mm | 600 mm de los extremos. Solo tramos laterales |

**Referencia añadida:**

| Ref.      | Descripción              | Precio |
| --------- | ------------------------ | ------ |
| 501111100 | Cinta transporte ventana | 0.12   |

### 3.3 Vínculos entre series

| Serie        | Descripción         | Precio |
| ------------ | ------------------- | ------ |
| Q65 HO + Q65 | Junta central P3153 | 0.12   |

### 3.4 Mecanizados Desagües

| Series                            | Tipo         | Ubicación                 |
| --------------------------------- | ------------ | ------------------------- |
| Todas las hojas, todas las series | Círculo 5 mm | Parte exterior de la hoja |

---

## 4. Solapes

### 4.1 Sin persiana

| Series                    | Solapes                        |
| ------------------------- | ------------------------------ |
| RM-75                     | 40033                          |
| RM40, Q60, Q65, Q77, RM60 | 1053 / Ángulos / 10362 / 10307 |
| Q95                       | 10307 / Ángulos / 10362        |

### 4.2 Con persiana

| Series              | Guía     | Solapes Laterales | Solape Inf. | Solape Sup. |
| ------------------- | -------- | ----------------- | ----------- | ----------- |
| RM-75               | Partidas | 40034             | 40033       | 40034       |
| RM-75               | 1102     | 40034             | 40033       | 40034       |
| RM-75               | Partidas | 10362             | 10362       | 10362       |
| RM40, Q60, Q65, Q77 | R1101    | 1054              | 1053        | 1054        |
| RM40, Q60, Q65, Q77 | R1102    | 1054              | 1053        | 1054        |
| RM40, Q60, Q65, Q77 | Partidas | 10362             | 10362       | 10362       |
| RM60                | R1101    | 1054              | 1053        | 1054        |
| RM60                | R1102    | 1054              | 1053        | 1054        |
| RM60                | 1102     | 1054              | 1053        | 1054        |

---

## 5. Consideraciones Importantes para Programación

* Si el producto va **con persiana**, el taladro superior en instalación obra **se desactiva**.
* El mecanizado de obra debe desplazarse cuando exista **recogedor de persiana**.
* Los mecanizados de cinta transporte solo se aplican en **tramos laterales**.
* Los solapes dependen de la **serie**, **si lleva persiana**, y el **tipo de guía**.

---

## 6. Próximos pasos

1. Definir las **tareas específicas** para programación.
2. Crear los archivos `.md` adicionales de tareas y pendientes.
3. Preparar los borradores de scripts siguiendo el flujo Codex → Taller.
