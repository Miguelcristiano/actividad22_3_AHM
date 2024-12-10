
# Instalación y Configuración del Tema Hello-4s3ti en Hugo

## Prerrequisitos

1. Tener [Hugo](https://gohugo.io/) instalado en tu sistema.
2. Contar con un proyecto Hugo ya inicializado:
   ```
   hugo new site nombre-del-sitio
   ```

![Sitio](/imagenes_cote/new.PNG)

## Instalación del Tema

### Opción 1: Clonando directamente
1. Accede al directorio de tu proyecto:
   ```
   cd nombre-del-sitio
   ```
2. Clona el repositorio del tema en la carpeta `themes/`:
   ```
   git clone https://github.com/4s3ti/hugo-theme-hello-4s3ti.git themes/hello-4s3ti
   ```

### Opción 2: Usando submódulos de Git
Para mantener el tema actualizado fácilmente:
1. Añádelo como submódulo:
   ```
   git submodule add https://github.com/4s3ti/hugo-theme-hello-4s3ti.git themes/hello-4s3ti
   ```

![Submodulo](/imagenes_cote/sub.PNG)

## Configuración Básica

1. Edita el archivo `config.toml` en la raíz y añade las siguientes configuraciones mínimas:
   ```
   baseurl      = "http://example.com/"
   title        = "Mi Blog"
   languageCode = "en-us"
   theme        = "hello-4s3ti"
   paginate     = 10

   [params]
     homeSubtitle = "Un blog simple y hermoso"
     enableSharingButtons = true
     description = "Mi nueva página web o blog"
     keywords = "blog, homepage"
   ```

![Conf](/imagenes_cote/toml.PNG)

2. (Opcional) Configuración de menús:
   ```
   [[menu.main]]
     identifier = "blog"
     name       = "Blog"
     url        = "/posts"
   ```

![Nav](/imagenes_cote/menu.PNG)

3. (Opcional) Copia el contenido de `exampleSite` incluido en el repositorio del tema para ver ejemplos:
   ```
   cp -r themes/hello-4s3ti/exampleSite/* .
   ```

## Visualización

1. Genera y prueba el sitio en un servidor local:
   ```
   hugo serve
   ```
2. Abre tu navegador en `http://localhost:1313`.

![Host](/imagenes_cote/iniciar.PNG)
