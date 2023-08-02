# db\_converter
Converting tool from BerkeleyDB to various databases formats

requires: libdb-devel, gdbm-devel, lmdb-devel, g++, make

## Build
* Clone the repo
* Build the binary `make`
## Usage
db\_converter --src SOURCE --dest DEST [ DBTYPE ]
* SOURCE - path to BerkeleyDB database
* DEST - file path to be created in the new database format
* DBTYPE - optional argument `--lmdb` for producing LMDB database.
GDBM is the default one. LMDB needs to have created directory for database files and provide it as parameter DEST

## Example
`./db_convert --src access.db --dest access.gdbm`

`mkdir lmdb`

`./db_convert --src access.db --dest lmdb --lmdb`
* Your new file with converted database will be created
