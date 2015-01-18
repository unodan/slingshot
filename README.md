# Slingshot

Automated Linux Package Installer for CentOS 7


Slingshot is a script to automate the installation and configuration of Linux software packages. Slingshot has and uses a template/messaging system.

You can use Slingshot to create custom server setups by writing script modules. Script modules should start by copying and modifying the Slingshot script temple module.

Slingshot was designed to be extended by simply adding new modules. Module scripts are added to a run queue and executed in (FIFO) order. You can create/add your own modules that customize package installation and/or configurations.

The use of modules allow you to extend or modify the system setup in ways that suit your particular needs.

The Slingshot base installs and configures the (Apache, MariaDB, PHP and NTP) packages and is a basic “LAMP” system. 

Below is the list of files that make up the base install of Slingshot. This list is the minimum set of files needed for a basic Slingshot (LAMP) installation.

<table>
<tr><th>File</th><th>Description</th>
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
</table>

