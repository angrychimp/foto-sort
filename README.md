# foto-sort
Somewhat simple PHP script to sort my photos for me.

### Dependencies
This project uses some submodules to fill library dependencies.
* [PHP-GetOpts](https://github.com/angrychimp/PHP-GetOpts) - Helps parse command-line options.
* [getID3](https://github.com/JamesHeinrich/getID3) - Provides functionality to get original capture date for an image.

These dependencies are included as sub-modules for the project. I could have likely had them included as part of some dependency manager thingy, but I figured this would be a good way for me to fiddle with submodules.

## Usage
`foto-sort [options] <dir|file>`  

    Options:
    -a | --action=(info|show|copy|move)     Specify the action to take
    -t | --target=<dir>                     Target folder when copying/moving files
    -n | --dry-run                          When copying/moving, just display the commands, don't actually copy/move anything.
    
    Actions:
    show|show-info|info                     Display full `getID3` output for file(s)
    move|copy                               Move or copy files from source to specified target
    list                                    Just list files, folders, decoded file type, and year/month (useful for determining if there are any duplicate filenames in your source tree)


