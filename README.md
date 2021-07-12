# nexus_xbot2
This package contains configuration files to control IIT's Nexus robot with the xbot2
RT middleware.

## Setup
1. make sure that hhcm's ethercat master is correcly installed and configured, i.e. running the command `repl` from command line results in the master running without errors
2. source the included `setup.sh` from the `.bashrc` file; this creates the alias `ecat_master`, to be used instead of directly calling `repl`; it internally calls `repl` with a proper configuration file for motors offsets and rotations signs that are specific to Nexus, and duplicates its standard output and standard error to the `/tmp/ecat-output` file

WARNING: calling `repl` directly must be avoided except for debugging purposes!

3. select the included basic configuration file for xbot2 with `set_xbot2_config <path-to-this-repo>/nexus_basic.yaml`

## Running the robot
The Nexus robot can be run from two terminals as follows:

- [terminal 1] `ecat_master`