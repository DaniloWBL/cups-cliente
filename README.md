# CUPS CLIENTES


Instalando um cliente de impressora no Linux

### Sobre 

CUPS (anteriormente um acrónimo para Common Unix Printing System, mas agora com nenhuma expansão oficial), um sistema de impressão para sistemas operativos de computador tipo unix, permite que um computador aja como um servidor de impressão.
-- Wikédia

Instação 
<pre>
sudo apt-get install cups
</pre>

Adicionar o usuário da máquina ao grupo de impressoras.
<pre>
usermod -a -G lpadmin username
</pre>

Liste os arquivos de instalação do Cups
<pre>
ls /etc/cups
</pre>

Entre na pasta
<pre>
cd /etc/cups
</pre>

Copie o arquivo de configuração do Cups
<pre>
cp cupsd.conf cupsd.old
</pre>

Edite o arquivo de configuração
<pre>
vi cupsd.conf
</pre>

Comente a aseguinte linha
<pre>
#Listen localhost:631 //comentando essa linha deixamos de escutar essa porta
</pre>

Abaixo de listen add a seguine linha de código
<pre>
port 631
</pre>

Altere o Location para esta forma add o comando abaixo dos que já existem
<pre>
location
Allow @local
/location

location /admin
Allow @local
/location

location /admin/conf
Allow @local
/location
</pre>

sai do arquivo
<pre>
:q para salvar :q!
</pre>

Reinicie  servidor
<pre>
/etc/init.d/cups restart
</pre>

Descubra o IP da máquina
<pre>
ifconfig 
</pre>

Acesso o sevidor no Navegador
<pre>
192.168.1.142:631 ou localhost:361
</pre>





