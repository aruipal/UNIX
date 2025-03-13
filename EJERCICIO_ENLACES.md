| <mark>Comando</mark> | <mark>Descripción</mark> |
| ----------- | ----------- |
| ln -s    | Crea enlace simbólico |
| ls  | Crea enlace duro |
| find /. -xtype l | Detectar enlaces |
| find /. -xtype l -delete | Borrar enlace |

## <ins>Tipos de archivos:</ins>
  - Ordinarios: archivos de texto o binarios.
  - Directorios: carpetas.
  - Enlaces punteros: punteros a otros archivos:
      - Duros: si el archivo se elimina sigue funcionando.
      - Simbólicos: como un acceso directo en windows. Si se borra el original el enlace queda roto.
### Ver tipo de archivo:
<pre><code id="codigo">file archivo.txt</code></pre>
### Crear enlace simbólico:
<pre><code id="codigo">ln -s /home/antonio/archivo.txt enlace_1</code></pre>
<pre><code id="codigo">ls -l enlace_1</code></pre>
### Crear enlace duro:
<pre><code id="codigo">ln archivo.txt enlace_2</code></pre>
### Detectar enlaces:
<pre><code id="codigo">find /home/antonio -xtype l</code></pre>
### Eliminar enlaces:
<pre><code id="codigo">find /home/antonio -xtype l -delete</code></pre>

### 1. Crear un archivo origen txt
<pre><code id="codigo">echo "Archivo de prueba" > origen.txt</code></pre>
### 2. Crear enlace duro llamado enlace_hard
<pre><code id="codigo">ln origen.txt enlace_hard</code></pre>
### 3. Crear enlace simbolico llamado enlace_soft
<pre><code id="codigo">ln -s origen.txt enlace_soft</code></pre>
### 4. Modificar origen.txt y observar cambios en los enlaces
<pre><code id="codigo">echo "Otra linea" >> origen.txt</code></pre>
<pre><code id="codigo">ls -l enlace_hard enlace_soft</code></pre>
### 5. Borrar origen txt y verificar que siguen funcionando
<pre><code id="codigo">rm origen.txt</code></pre>
<pre><code id="codigo">cat enlace_hard</code></pre>
<pre><code id="codigo">cat enlace_soft</code></pre>
<pre><code id="codigo">ls -l enlace_hard enlace_soft</code></pre>
### Detectar enlaces
<pre><code id="codigo">find . -xtype l</code></pre>
### Eliminar enlaces rotos
<pre><code id="codigo">find . -xtype -delete</code></pre>
### Crear archivo, generar enlaces y mostrar información:
  <pre><code id="codigo">echo "Esto es un archivo" > origen.txt</code></pre>
  <pre><code id="codigo">ln origen.txt enlace1</code></pre>
  <pre><code id="codigo">ln -s origen.txt enlace2</code></pre>
  <pre><code id="codigo">ls -li enlace1 enlace2</code></pre>
