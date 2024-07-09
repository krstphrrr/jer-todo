## 2024-07-08
- DIMA
  - [ ] ensure bigger dimas (NDOW) can be ingested using the accdb to csv method **PRIORITY #3**
  - [ ] test in local environment for Brandi **PRIORITY #2**
  - wishlist: refactor command line part

- API
  - [ ] update permissions to remove ndow: aws plugin, .env file, PG connection functions etc. 
  - [ ] update the cognito:groups on the AWS dashboard
  - [ ] adopt LEGAL / PUBLICATION framework for permissions

- TALL TABLE
  - [ ] ingest tblRHEM **PRIORITY #1**
  - wishlist: refactor command line part


- LDC DB
  - [ ] script to modify tables to have their DBIngestedIn column be autopopulated on ingestion
  - [ ] develop separate DB/schema with a github actions tracked "latest" schemaplan. 
  - [ ] develop SQL function to read the latest schemaplan to keep the database structure up to date
  - [ ] go with 1.1.9 csv: create a python script to pull csv from 
  - [ ] clean up the semver folder: archive directory and latest one outside
  
  - [ ] Stone Enviorenmental layers
    - [ ] restore geoserver on jornada.nmsu
    - [ ] ingest 30+ 4k rasters to ldc database
