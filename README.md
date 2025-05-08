# 🐳 Introducción a Docker

## ¿Qué es Docker?

Docker es una plataforma de código abierto que permite desarrollar, empaquetar y ejecutar aplicaciones dentro de **contenedores**. Un contenedor es una unidad estándar de software que agrupa el código de una aplicación y todas sus dependencias, asegurando que esta se ejecute de forma **rápida, consistente y portátil** en cualquier entorno.

## ¿Por qué usar Docker?

Antes de Docker, los desarrolladores solían decir:  
> “Funciona en mi máquina…”

Con Docker, ese problema desaparece, porque los contenedores se comportan de la misma manera, sin importar dónde se ejecuten: tu PC, un servidor, o la nube.

### Ventajas principales:

- ✅ **Portabilidad**: corre igual en cualquier sistema que tenga Docker instalado.
- 🔒 **Aislamiento**: cada contenedor es independiente del sistema y de otros contenedores.
- 🚀 **Velocidad**: los contenedores son más ligeros y rápidos que las máquinas virtuales.
- 🔁 **Reproducibilidad**: ideal para CI/CD y despliegues consistentes.
- 🧪 **Ambientes de desarrollo limpios**: sin instalar múltiples versiones de librerías o bases de datos en tu sistema.

## ¿Qué es un contenedor?

Un contenedor es como una “caja” que contiene tu aplicación + dependencias + configuraciones necesarias para ejecutarse.

Un contenedor se basa en una **imagen**, que es como una plantilla inmutable con todo lo necesario para crear instancias (contenedores).

## ¿Cómo funciona Docker?

1. 🛠️ El desarrollador escribe un **Dockerfile** con las instrucciones para construir una imagen.
2. 🧱 Docker construye una **imagen** con el código y sus dependencias.
3. 🚢 Se ejecuta un **contenedor** a partir de esa imagen.
4. 🔄 El contenedor puede iniciarse, detenerse, reiniciarse o eliminarse fácilmente.

## Componentes clave

| Componente       | Descripción                                                                 |
|------------------|-----------------------------------------------------------------------------|
| Docker Engine     | Servicio que ejecuta y gestiona contenedores.                              |
| Imagen (Image)    | Plantilla de solo lectura usada para crear contenedores.                   |
| Contenedor        | Instancia ejecutable de una imagen.                                        |
| Dockerfile        | Archivo de texto que define cómo construir una imagen personalizada.       |
| Volumen           | Espacio de almacenamiento persistente entre contenedores.                  |
| Red               | Sistema que permite la comunicación entre contenedores o con el exterior.  |
| Docker Compose    | Herramienta para definir y correr múltiples contenedores con un solo comando. |

## Comparación: Docker vs Máquina Virtual

| Característica       | Docker (Contenedores)       | Máquina Virtual             |
|----------------------|-----------------------------|-----------------------------|
| Tamaño               | Ligero (~MB)                | Pesado (~GB)                |
| Inicio               | Rápido (segundos)           | Lento (minutos)             |
| Aislamiento          | A nivel de proceso          | A nivel de sistema operativo|
| Rendimiento          | Alto                        | Menor debido a la emulación |
| Portabilidad         | Muy alta                    | Limitada                    |

## Ejemplo básico: Ejecutar un contenedor

```bash
# Ejecutar un contenedor con Nginx
docker run -d -p 8080:80 nginx
