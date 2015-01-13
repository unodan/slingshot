# Slingshot

Automated Linux Package Installer for CentOS 7

Slingshot is a script to automate the installation and configuration of Linux software packages. Slingshot has and uses a template/messaging system.

You can use Slingshot to create custom server setups by writing script modules. Script modules should start by copying and modifying the Slingshot script temple module.

The Slingshot base installs and configures the (Apache, MariaDB, PHP and NTP) packages and is a basic “LAMP” system.

Slingshot was designed to be extended easily by adding new module scripts. Module scripts are placed in the run queue to be executed at specific time. 

Slingshot allows you to add your own custom packages and/or configurations that modify the base system to suit your needs.

The base install of Slingshot consists of 12 scripts, plus the install script. 

Placing a module in the scripts directory means that script will be include in the run queue, “the script must use the Slingshot template system to be included!”.

Below is the list of files that make up the base install of Slingshot. This list is the minimum set of files needed for a basic (LAMP) Slingshot installation.

<table>
<tr><td>settings</td><td>Custom settings file, unique to your setup.</td>
<tr><td>install</td><td>Starts the local installation from a Linux system.</td>
<tr><td>setup</td><td>This script is started by install script stated above or can be started manually.</td>
<tr><td>installer</td><td>The module that queues scripts that get installed on the host target system.</td>
<tr><td>user</td><td>Sets up the default user account on the target system.</td>
<tr><td>ntp</td><td>Installs and configures the NTP client.</td>
<tr><td>network</td><td>Configures the network interface and network settings.</td>
<tr><td>httpd</td><td>Installs and configures the Apache Web Server.</td>
<tr><td>mariadb</td><td>Installs and configures the MariaDB SQL Server.</td>
<tr><td>php</td><td>Installs and configures PHP.</td>
<tr><td>constants</td><td>Constants used for controlling program execution and error handling.</td>
<tr><td>functions</td><td>Helper functions used by various scripts.</td>
<tr><td>template	</td><td>A template script used as a starting point for new scripts modules.</td>
</table>

