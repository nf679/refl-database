# Reflectometry Database 

A mongodb database containing parameters for materials used in reflectometry, and their reflectivity parameters. The values used to create informed and uniform priors are included for the relevant parameters.
The following parameters are currently included  (with the italic parameters having prior values available): 
  
**Molecular parameters:**
  * CAS number
  * _Molecular volume_
  * Molecular weight
  * Molecular scattering length density
  * _Area per molecule_
  
**Amphiphile parameters:**
  * _Head volume_
  * _Tail volume_
  * Head scattering length
  * Tail scattering length
  
**Phospholipid parameters:**
  * Natural or synthetic?
  
**Reflectivity parameters:**
  * _Tail thickness_
  * _Head thickness_
  * _Roughness_
  * _phi_h (check what this is?)_
  * _phi_t (check what this is?)_


## Examples of using the database: 

* **To build the database, type in the terminal (not a mongo shell):**

cd refl-database-main

mongorestore --db refl_database db/dump/refl_database

* **To check whether the collections were imported successfully:**

mongo

show dbs

use refl_database

show collections 

* **To show the entries in a collection, for example in the amphiphiles collection:**

db.amphiphiles.find({})

* **To show how many entries there are in a collection, e.g. how many phospholipids there are:**

db.phospholipids.count()
