# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name <nombre contenedor> <nombre imagen>:<tag>
```
Crear el contenedor  **srv-web** usando la imagen nginx version alpine
<img width="525" height="121" alt="image" src="https://github.com/user-attachments/assets/32374435-6038-4081-a512-700a5545f58d" />

# COMPLETAR

Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world
<img width="976" height="313" alt="image" src="https://github.com/user-attachments/assets/d9e8d817-fb25-410f-a683-ad296c26e06f" />

# COMPLETAR

### Listar los contenedores ejecutándose o no

```
docker ps -a
```
<img width="974" height="213" alt="image" src="https://github.com/user-attachments/assets/26bb247b-8f04-468a-be65-1d9b7d0ed9d0" />

### Para iniciar un contenedor

```
docker start <nombre contenedor o identificador>
```
Iniciar el contenedor srv-web 
<img width="300" height="131" alt="image" src="https://github.com/user-attachments/assets/cab54bc0-1b3f-4044-a188-91c6a20ef762" />

# COMPLETAR

### Listar los contenedores ejecutándose
```
docker ps 
docker ps | grep <nombre contenedor>
```

### Para detener un contenedor

```
docker stop <nombre contenedor>
```

### Para crear un contenedor y ejecutarlo inmediatamente

```
docker run --name <nombre contenedor> <nombre imagen>:<tag>
```
![Ecosistema de Docker](dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine
<img width="976" height="570" alt="image" src="https://github.com/user-attachments/assets/ec23a5d7-2db0-46a7-a628-f005d011e63f" />

# COMPLETAR

**¿Qué sucede luego de la ejecución del comando?**
1. Descarga (si no existe): Docker busca la imagen nginx:alpine en PC. Si no la encuentra, la baja de internet.
2. Crea y Nombra: Crea un contenedor nuevo basado en la imagen nginx:alpine y le pone el nombre srv-web2.
3. Arranca el proceso: Inicia el servidor Nginx y bloquea el terminal para mostrar los logs.

# COMPLETAR  

Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine
<img width="524" height="113" alt="image" src="https://github.com/user-attachments/assets/7cae488e-449d-4874-a114-cefd8287e19b" />

# COMPLETAR

### Para eliminar un contenedor

```
docker rm <nombre contenedor>
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 
<img width="360" height="117" alt="image" src="https://github.com/user-attachments/assets/d6ac4277-f422-45e3-ac72-80b7a108fd20" />

# COMPLETAR

Verificar que el contenedor que se eliminó
<img width="845" height="128" alt="image" src="https://github.com/user-attachments/assets/0855bf4e-af32-4b06-8945-5fa4b7d0d7ac" />

# COMPLETAR

### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f <nombre contenedor>
```
Eliminar el contenedor **srv-web3** 
<img width="314" height="142" alt="image" src="https://github.com/user-attachments/assets/ade0dd79-31f8-4fa4-bf26-b4ecdaf9817c" />

# COMPLETAR

Verificar que el contenedor que se eliminó
<img width="975" height="181" alt="image" src="https://github.com/user-attachments/assets/90d9fa88-f0cb-4346-bcc0-5cf591b679ed" />

# COMPLETAR

### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web** 
# COMPLETAR
