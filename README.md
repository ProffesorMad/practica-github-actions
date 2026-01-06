# Práctica GitHub Actions – CI Básico

## Descripción
Este repositorio contiene una GitHub Action creada desde cero como parte de la práctica de la asignatura **Despliegue de Aplicaciones Web**.

La práctica consiste en la creación y análisis de un workflow de **Integración Continua (CI)** sencillo utilizando **GitHub Actions**, con el objetivo de comprender su estructura, funcionamiento y ejecución.

---

## Objetivo de la práctica
Los objetivos principales de esta práctica son:

- Comprender qué son las GitHub Actions y para qué se utilizan
- Aprender la estructura básica de un workflow definido en YAML
- Analizar cómo se ejecutan los jobs y steps
- Visualizar y entender los logs de ejecución
- Automatizar una tarea sencilla al realizar cambios en el repositorio

---

## Ubicación del workflow
Los workflows de GitHub Actions deben almacenarse dentro del repositorio en la siguiente ruta:  .github/workflows/

En este proyecto, el archivo del workflow es:  ci.yml


GitHub detecta automáticamente este archivo y ejecuta la acción cuando se cumple el evento configurado.

---

## Descripción general del workflow

### Nombre del workflow

CI - Hola GitHub Actions


Este nombre es el que aparece visible en la pestaña **Actions** del repositorio.

---

### Evento de ejecución
El workflow se ejecuta automáticamente cuando se produce el siguiente evento:

- **push** a la rama `main`

Esto permite que la acción se ejecute cada vez que se suben cambios al repositorio.

---

## Job y entorno de ejecución

El workflow define un único job con las siguientes características:

- **Nombre del job:** saludo
- **Sistema operativo:** ubuntu-latest

El job se ejecuta en una máquina virtual Linux proporcionada por GitHub, sin necesidad de configuración adicional.

---

## Steps del workflow

El job ejecuta los siguientes pasos en orden:

### 1. Mostrar mensaje
- Ejecuta un comando mediante `run`
- Utiliza el comando `echo` para imprimir un mensaje en los logs
- Permite comprobar visualmente que la GitHub Action se ha ejecutado correctamente

Este step sirve como verificación básica del correcto funcionamiento del workflow.

---

## Ejecución del workflow

Una vez realizado un `git push` al repositorio, el workflow se ejecuta automáticamente.

La ejecución finaliza en estado **Success**, lo que indica que el job y todos sus steps se han completado sin errores.  
El mensaje generado por el comando `echo` puede observarse en los logs de la ejecución.

---

## Evidencias
La correcta ejecución del workflow puede comprobarse en la pestaña **Actions** del repositorio, donde se muestran:

- El estado de la ejecución
- El job ejecutado
- Los steps completados
- Los logs generados durante la ejecución

---

## Conclusiones
GitHub Actions es una herramienta muy potente para automatizar tareas dentro del ciclo de desarrollo de software.

Mediante esta práctica se ha podido comprobar cómo crear una GitHub Action desde cero, definir un workflow sencillo y analizar su ejecución, sentando las bases para la creación de flujos de CI/CD más complejos en proyectos reales.
