### Crea un grupo llamado E2T:
<pre><code id="codigo">sudo groupadd E2T</code></pre>
### Añade 3 usuarios al grupo:
<pre><code id="codigo">sudo usermod -aG E2T antonio</code></pre>
<pre><code id="codigo">sudo usermod -aG E2T aruipal</code></pre>
<pre><code id="codigo">sudo usermod -aG E2T Armada_ESP</code></pre>
### Dale propietario al archivo.txt uno de los 3 del punto anterior y añadelo a otro grupo:
<pre><code id="codigo">sudo chwon aruipal archivo.txt</code></pre>
### Muestrame los grupos del usuario que añadisteis en el punto anterior:
<pre><code id="codigo">groups aruipal</code></pre>
<pre><code id="codigo">cat /etc/group</code></pre>
