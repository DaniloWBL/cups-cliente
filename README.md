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



