# Bash scripts

## Using `set` ([1](https://vaneyckt.io/posts/safer_bash_scripts_with_set_euxo_pipefail/), [2](https://www.gnu.org/software/bash/manual/html_node/The-Set-Builtin.html))
- `set -e`/`set -o errexit`: abort script if any line of commands exits with a non-zero status; performs code set as a trap for `ERR`
- `set -u`/`set -o nounset`: upon encountering an unset variable the script is terminated with a message
- `set -x`/`set -o xtrace`: for debugging purposes first echo every line before it is executed
- `set -E`/`set -o errtrace`: use together with `-e` to allow the trap to fire even if the problem occurs inside another function
- `set -o pipefail`: return value of a pipeline is the rightmost non-zero value or zero if all commands exit with zero

## Traps ([1](http://tldp.org/LDP/Bash-Beginners-Guide/html/sect_12_02.html))
- `trap "<code>" SIGINT`: `<code>` is executed when the program receives a keyboard interrupt
