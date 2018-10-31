glpi-9.3.2

GLPI 9.3.2 en Centos 7

Una forma sencilla de instalar GLPI en CentOS 7.

# Antes de instalar la versión MariaDB 10.0 es importante remover la versión 5.5 del MariaDB.

yum remove mariadb-server mariadb-libs

# Creación de repositorio de MariaDB en el CentOS

vi /etc/yum/yum.repos.d/mariadb.repo

#MariaDB 10.0 CentOS repository list – created 2014-09-29 14:57 UTC

#http://mariadb.org/mariadb/repositories/

[mariadb]

name = MariaDB

baseurl = http://yum.mariadb.org/10.0/centos7-amd64

gpgkey=https://yum.mariadb.org/RPM-GPG-KEY-MariaDB

gpgcheck=1


Requerimientos: Debes tener instalado git para descargar este repositorio: sudo yum -y instalar git

Descargar el script: git clone https://github.com/dsegurag/centos-glpi.git

Posteriormente ingrese: cd centos-glpi

Y luego ejecute: chmod + x install-glpi.sh

Instalación: ./install-glpi.sh

•	Cosas para cambiar en el Script.

Cuando cree el usuario para la base de datos, se recomienda encarecidamente cambiar la contraseña predeterminada. Reemplace la contraseña por su propia contraseña segura.

En la parte de host virtual, debe cambiar el valor glpi.domain.local por su dominio deseado.
