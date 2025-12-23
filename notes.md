The configuration file is handled in src\pc\configfile.c and the default config load, if something is bad, is done in line 829.

To reset the bindings to default, we would just load the existing configuration again. Let's try it?

I'll need to have configfile.h available

Another idea is to replace the block of controller mapping from backup to actual configuration.
See configfile_load_internal in configfile.c for CONFIG_TYPE_BIND. I could use a similar logic to copy just that block. Although perhaps an easier starting place would be replacing the whole thing.