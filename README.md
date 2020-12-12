# dockerbox

Notas sobre la instalación de dockerbox.

## Instalar Docker en Windows 10

Windows 10 Pro:

![](imagenes/Anotación_2020-12-12_120421.png)

Descargar e instalar:

![](imagenes/Anotación_2020-12-12_120706.png)

![](imagenes/Anotación_2020-12-12_120736.png)

![](imagenes/Anotación_2020-12-12_121111.png)

![](imagenes/Anotación_2020-12-12_121212.png)

![](imagenes/Anotación_2020-12-12_121646.png)

Instalar el paquete WSL:

![](imagenes/Anotación_2020-12-12_121949.png)

![](imagenes/Anotación_2020-12-12_122124.png)

![](imagenes/Anotación_2020-12-12_122147.png)

Reiniciar:

![](imagenes/Anotación_2020-12-12_122220.png)

Arranque de Docker:

![](imagenes/Anotación_2020-12-12_122247.png)

![](imagenes/Anotación_2020-12-12_122429.png)

## Instalar make

Chocolatey:

![](imagenes/Anotación_2020-12-12_123157.png)

Make:

![](imagenes/Anotación_2020-12-12_123400.png)

## Error de credential-desktop

Si da este error al arrancar:

```text
docker.errors.DockerException: Credentials store error: StoreError('Credentials store docker-credential-desktop exited with "error getting credentials - err: exit status 1, out: `No se ha encontrado el elemento.`".')
```

Editar el fichero:

```text
C:\Users\<usuario>\.docker\config.json
```

Y comprobar que el valor `credStore` aparece una sola vez:

```json
{"credStore":"desktop","stackOrchestrator":"swarm"}
```

## Arrancar los contenedores de dockerbox

![](imagenes/Anotación_2020-12-12_123433.png)

![](imagenes/Anotación_2020-12-12_125631.png)

La primera vez hay que esperar a que genere la clave privada:

![](imagenes/Anotación_2020-12-12_125802.png)

![](imagenes/Anotación_2020-12-12_130258.png)

Los certificados son autofirmados:

![](imagenes/Anotación_2020-12-12_130437.png)

![](imagenes/Anotación_2020-12-12_130511.png)

## Reducir el consumo de memoria

[WSL2 Tips: Limit CPU/Memory When using Docker](https://itnext.io/wsl2-tips-limit-cpu-memory-when-using-docker-c022535faf6f)

Crear el fichero:

```text
C:\Users\<usuario>\.wslconfig
```

Y poner en él:

```ini
[wsl2]
memory=1GB
processors=2
```

![](imagenes/Anotación_2020-12-12_131426.png)

![](imagenes/Anotación_2020-12-12_131810.png)
