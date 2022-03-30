# batchprimer3-documented

### REQUIREMENTS OF BATCHPRIMER3
Language: Perl interpreter program, Perl 5.8 or above.<br>
HTTP Server: Apache HTTP server.<br>
Perl package: The following Perl packages are needed:<br>
FileHandle<br>
IPC::Open3<br>
Carp<br>
CGI<br>
Socket<br>
GD::Graph::bars<br>
GD::Graph::colour<br>
GD::Text<br>
POSIX <br>
Email::Valid<br>
Thread<br>

### INSTALLATION

Here are the installation instructions for Linux system.

1. Git Clone

2. Copy the "batchprimer3_cgi" directory to your Apache server "cgi-bin" directory, change the folder name to "batchprimer3".
chmod 777 *

3. Copy the "batchprimer3_htdocs" directory to your Apache server "htdocs" directory and 
rename the directory to "batchprimer3".
chmod 777 *

4. In the /cgi-bin/batchprimer3/ directory, you need to correctly set the parameters in two 
programs, batchprimer3.cgi and batchprimer3_report.cgi. Please carefully check the 
header part in these two files.

5. Replace:<br>
&#60;Directory&#62;<br>
  AllowOverride none<br>
  Require all denied<br>
&#60;/Directory&#62;<br>
<br>to:<br><br>&#60;Directory "/www/server/htdocs/cgi-bin/"&#62;<br>
  AllowOverride None<br>
  Options +ExecCGI<br>
  Order allow,deny<br>
  Allow from all<br>
&#60;/Directory&#62;<br>
