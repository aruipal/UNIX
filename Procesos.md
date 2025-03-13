### Ver procesos
<pre><code id="codigo">ps aux</code></pre>
- Por usuario:
<pre><code id="codigo">ps -u antonio</code></pre>
- En tiempo real:
<pre><code id="codigo">top</code></pre>
### Eliminar proceso por PID
<pre><code id="codigo">kill 851</code></pre>
- A lo bruto:
<pre><code id="codigo">kill -9 851</code></pre>
### Procesos en 2º plano
<pre><code id="codigo">jobs</code></pre>
- Mandar proceso a foreground (1 plano):
<pre><code id="codigo">fg %1</code></pre>
- Mandar proceso a background (2º plano):
<pre><code id="codigo">fg %2</code></pre>
### Matar el último proceso
<pre><code id="codigo">kill %1</code></pre>
### Eliminar procesos de usuario
<pre><code id="codigo">pkill -u antonio</code></pre>
### Eliminar procesos de un tipo
<pre><code id="codigo">pkill firefox</code></pre>
