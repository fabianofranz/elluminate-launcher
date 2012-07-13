Elluminate Launcher
===================

Launch an Elluminate session from the command line:

    elluminate 'https://sas.elluminate.com/m.jnlp?sid=000&password=0.012345678901234567890123456789'

This script will properly set `LD_LIBRARY_PATH` (required to launch Elluminate using OpenJDK 7), clear Web Start cache, besides other things.

You can define your full name using the env var `elluminate_user_name`.