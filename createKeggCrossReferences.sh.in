#!/bin/bash
# Parse the mapping of EC-numbers onto KEGG-pathways.

set -o pipefail -e
exec 3>&1

mapping=http://rest.kegg.jp/link/path/ec

lines="$(wget -q "$mapping" -O - | nl -s "  " | tee >(cat >&3))"

