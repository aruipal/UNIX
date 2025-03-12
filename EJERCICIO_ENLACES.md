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
