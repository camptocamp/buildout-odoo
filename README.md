# buildout-odoo

Base of buildout recipe for odoo servers and development computers.

## Extends your project's configuration

Your project will have at least one `common.cfg` with the base configuration,
and one additional file per environment (`dev.cfg`, `prod.cfg`, ...).

The `common.cfg` file must contain this option:

```
[buildout]
extends = https://raw.githubusercontent.com/camptocamp/buildout-odoo/master/default.cfg?token=8393502__eyJzY29wZSI6IlJhd0Jsb2I6Y2FtcHRvY2FtcC9idWlsZG91dC1vZG9vL21hc3Rlci9kZWZhdWx0LmNmZyIsImV4cGlyZXMiOjE0MDk4Mjg4NTd9--5fd20d8b5834d84491bf069ab081a9e5b127f114
```

## Bootstrapping OpenERP / Odoo

Clone the project's branch:

```bash
git clone git@github.com:camptocamp/your_project.git -b the_required_branch
```

Create a `buildout.cfg` symlink to the environment file you want to use:

```bash
ln -s dev.cfg buildout.cfg
```

Bootstrap:

```bash
./bootstrap.sh
bin/buildout
```

For more details please refer to : http://doc.business.internal/technical/
