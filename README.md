buildout-odoo
=============

Base of buildout recipe for odoo servers.

To be deployed as ~/.buildout


You may want to manually create ~/.buildout/local.cfg which will be sourced if
present. It can be used to declare a local shared directory for eggs, such as:

    [buildout]
    eggs-directory = /home/<yourlogin>/.eggs-cache
