# groups.io-imports
 Import scripts for Groups.io

This set of import scripts is based on the [Groups.io Yahoo import script](http://lena.kiev.ua/ioimport.zip) from the [Groups.io Group Managers Forum](https://groups.io/g/GroupManagersForum/message/22251). The original Yahoo script here is hers.

# History

2020-03-28: Updated naming convention and instructions
2020-03-08: Initial commit with yahoo.ioimpport.pl v7

# Usage Instructions

Each script will have its own usage instructions within it. Scripts are identified with the naming convention `{source}.{destination}.{extension}`. For example:

* `yahoo.groupsio.pl` - A Perl script that reads exported files from Yahoo and imports them to groups.io
* `sympa.mbox.bash` - A Bash script that reads exports from Sympa and creates MBOX files