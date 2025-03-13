| <mark>Comando</mark> | <mark>Descrición</mark> |
| ----------- | ----------- |
| groupadd    | Crea grupo |
| useradd -m  | Crea usuario |
| passwd      | Crea contraseña |
| usermod -aG | Añade usuario a grupo |
| userdel -r  | Borra usuario |
| chown       | Cambiar propietario |
| groups      | Mostrar grupos del usuario |

### Crea un grupo llamado E2T:
<pre><code id="codigo">sudo groupadd E2T</code></pre>
### Crea un usuario:
<pre><code id="codigo">sudo useradd -m aruipal</code></pre>
### Contraseña de usuario:
<pre><code id="codigo">sudo passwd aruipal</code></pre>
### Añade 3 usuarios al grupo:
<pre><code id="codigo">sudo usermod -aG E2T antonio</code></pre>
<pre><code id="codigo">sudo usermod -aG E2T aruipal</code></pre>
<pre><code id="codigo">sudo usermod -aG E2T Armada_ESP</code></pre>
### Borra un usuario:
<pre><code id="codigo">sudo userdel -r Armada_ESP</code></pre>
### Dale propietario al archivo.txt uno de los 3 del punto anterior y añadelo a otro grupo:
<pre><code id="codigo">sudo chwon aruipal archivo.txt</code></pre>
### Muestrame los grupos del usuario que añadisteis en el punto anterior:
<pre><code id="codigo">groups aruipal</code></pre>
<pre><code id="codigo">cat /etc/group</code></pre>

