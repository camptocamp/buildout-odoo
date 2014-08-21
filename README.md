buildout-odoo
=============

Base of buildout recipe for odoo servers.

To be deployed as ~/.buildout


You may want to manually create ~/.buildout/local.cfg which will be sourced if
present. It can be used to declare a local shared directory for eggs, such as:

    [buildout]
    eggs-directory = /home/<yourlogin>/.eggs-cache

Bootstrapping OpenERP
---------------------

You need to checkout the base buildout config at the root of curent user home

  ```bash
  cd ~/
  git clone git@github.com:camptocamp/buildout-odoo.git .buildout
  ```

Then move to your instance location and clone project branch
  ```bash
  git clone git@github.com:camptocamp/your_project.git -b the_required_branch
  ```

Then boostrap the instance
  ```bash
   ./bootstrap.sh
   bin/buildout
  ```

For more details please refer to : http://doc.business.internal/technical/
