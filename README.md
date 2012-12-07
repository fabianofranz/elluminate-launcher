Elluminate Launcher
===================

Small and stupid script to launch an Elluminate session from the command line:

    elluminate 'https://sas.elluminate.com/m.jnlp?sid=000&password=0.012345678901234567890123456789'

This script will download the JNLP file, set your username, and launch
the session.

ENV Variables
=============
## Username
Your username can be overridden by setting
`ENV['elluminate_user_name']`.
Otherwise, your system username (`ENV['USER']`) is used.

## Launch Command
This is the command that is run when launching the file.
This defaults to to `javaws.itweb`.
You can change it by setting `ENV['elluminate_cmd'].

## Exports
This allows you to set exports before running the command.
Use this if you need to alter your `LD_LIBRARY_PATH`.

For instance,
`export elluminate_export="LD_LIBRARY_PATH=${LD_LIBRARY_PATH:+$LD_LIBRARY_PATH:}/usr/lib/jvm/jre-1.7.0-openjdk.x86_64/lib/amd64"`

## Debug
This prints out more useful debugging information.
Set `ENV['DEBUG']` = 1.

Example
=======

```
DEBUG=1 elluminate_user_name=me elluminate_cmd=/usr/bin/javaws.itweb elluminate_export="LD_LIBRARY_PATH=${LD_LIBRARY_PATH:+$LD_LIBRARY_PATH:}/usr/lib/jvm/jre-1.7.0-openjdk.x86_64/lib/amd64" elluminate <url>
```
