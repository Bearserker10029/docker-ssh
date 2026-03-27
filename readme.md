hola gaaaaaaa
=======
# Ubuntu + Git Docker Environment
gooooo
## Descripción

Este proyecto define una imagen Docker basada en Ubuntu que incluye Git instalado y el sistema actualizado. El objetivo es proporcionar un entorno reproducible para practicar comandos básicos de Docker y Git.

---

## Requisitos

Antes de comenzar, asegúrate de tener instalado:

* Docker
* Git

---

## Estructura del proyecto

```
.
├── Dockerfile
└── README.md
```

---

## Construcción de la imagen

Ubícate en la raíz del proyecto y ejecuta:

```
docker build -t ubuntu-git .
```

Este comando construye una imagen llamada `ubuntu-git` utilizando el Dockerfile.

---

## Ejecución del contenedor

Para iniciar el contenedor en modo interactivo:

```
docker run -it ubuntu-git
```

Una vez dentro del contenedor, puedes verificar que Git está instalado:

```
git --version
```

---

## Comandos útiles dentro del contenedor

Actualizar lista de paquetes:

```
apt-get update
```

Verificar versión de Git:

```
git --version
```

Configurar Git:

```
git config --global user.name "Tu Nombre"
git config --global user.email "tu@email.com"
```

---

## Flujo completo

```
git clone <URL_DEL_REPOSITORIO>
cd <NOMBRE_DEL_PROYECTO>
docker build -t ubuntu-git .
docker run -it ubuntu-git
```

---

## Posibles errores

* El contenedor se cierra inmediatamente
  Asegúrate de usar `-it` al ejecutar `docker run`.

* Error al instalar paquetes
  Verifica que el Dockerfile incluya `apt-get update` antes de instalar.

* Permisos de Docker
  Ejecuta Docker con permisos adecuados o agrega tu usuario al grupo docker.

---

## Objetivos de aprendizaje

* Comprender la estructura de un Dockerfile
* Construir imágenes Docker
* Ejecutar contenedores
* Utilizar Git dentro de un entorno aislado

---

## Ejercicio sugerido

1. Modifica el Dockerfile para instalar también curl.
2. Reconstruye la imagen.
3. Ejecuta el contenedor y verifica la instalación con:

```
curl --version
```

---

## Autor

Proyecto utilizado con fines educativos.
