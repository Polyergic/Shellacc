# Paths

A weak suggestion for an FHS-like allocation of paths in $HOME

- `~/bin` - executable commands

- `~/lib` - library code used by commands in ~/bin

- `~/lib/$name/data` - static data used by the $name library

- `~/etc` - configurations

- `~/var` - persistent state information (usually not safe to delete)

- `~/tmp` - transient state information (automatically deleted at reboot)

- `~/cache` - cached data (safe to delete when program is not running)

- `~/hosts/$HOSTNAME/$above` - host-specific variants of above

**Note contrast with other implementations**

- XDG Desktop pathes
 
  https://specifications.freedesktop.org/basedir-spec/basedir-spec-latest.html#basics
   
  - Single hidden dir is better than hidden dir per tool

  - Does not separate config from state

  - No mechanism for multiple hosts
