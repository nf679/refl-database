# Reflectometry Database 

A mongodb database containing parameters for materials used in reflectometry, and their reflectivity parameters. 
The following parameters are currently included: 
  
**Molecular parameters:**
  * CAS number
  * Molecular volume
  * Molecular weight
  * Molecular scattering length density
  * Area per molecule
  
**Amphiphile parameters:**
  * Head volume
  * Tail volume
  * Head scattering length
  * Tail scattering length
  
**Phospholipid parameters:**
  * Natural or synthetic?
  
**Reflectivity parameters:**
  * Tail thickness
  * Head thickness
  * Roughness
  * phi_h (check what this is?)
  * phi_t (check what this is?)


## Examples of using the database: 

**To build the database, type in the terminal (not a mongo shell):**

mongorestore --db refl_database db/dump

**To check whether the collections were imported successfully:**

mongo

show dbs

use refl_database

show collections 

**To show the entries in a collection, for example in the amphiphiles collection:**

db.amphiphiles.find({})
