## 2024-07-08
- runners (x.174)
  - [x] create sidecar docker in docker compose file
  - [x] determine if there is any port access issue between x.174 and github. Does it have to be proxied by web (x.153)?
  - [x] create runner with sidecar
    - [x] migrate JER runner from x.187 to x.174
    - [x] migrate LDC runner from x.184 to x.174 

- RMA/AGRisk (x.148)
  - [x] resolve script to update db 

- new LDC (x.154)
  - currently running fastify API.
  - proxied through x.153
  - required domain change at NMSU netreg from x.184 to x.153.
  - queries data from HA Proxy at x.153, which in turn queries from pgbnc-1  (x.216) or on pgbnc-2(x.188), which in turns queries from LDCDB either on ldcdb-1 (x.155) or ldcdb-2 (x.188) 

- LDCDB
  - [ ] complete the logical replication from ldcdb x.155 to x.188
    - wishlist: ansible playbook 
    - wishlist: leverage the github runners to update functions/procedures while also keeping track of changes
      - sql file would include version within the function declaration (not name otherwise we would have every iteration of a function available on the db, we would rather just replace a single one while also have a record of which version it is inside the function declaration)
      - db-update user would run the update or replace function from appleboy/ssh-master on commits.

- AIM (x.158)
  - [x] migrate from k8s (x.140) to aim (x.158)
    - [x] download physical backup of site
    - [x] update netreg entry from x.140 to web (x.153)
  

- learn (x.157)
  - [x] migrate from k8s (x.140) to learn (x.157)
    - [x] download physical backup of site
    - [x] update netreg entry from x.140 to web (x.153)

- landscape toolbox (x.156)
  - [x] migrate from k8s (x.140) to learn (x.156)
    - [x] download physical backup of site
    - [x] update netreg entry from x.140 to web (x.153)
    
- western snow conf (x.217)
  - [x] migrate from k8s (x.140) to learn (x.217)
    - [x] download physical backup of site
    - [x] update netreg entry from x.140 to web (x.217)

- apps (x.159)
  - [x] migrate from swb-apps (x.169) to apps (x.159)
    - [x] update apache entry on x.139 

- rap (x.175) 
  - [ ] migrate from LDC2 (x.184) to rap (x.175)
  - [ ] update domain registration with web (x.153) - squarespace
  - [ ] update angular image to latest (17+) after migration
  - [ ] update CICD script

- web (x.153)
  - proxies databases using HA Proxy 
  - proxies other web apps through nginx into public internet through 443
  -  collects logs from other docker setups and exposes that endpoint on a jornada subdomain. 
  - [x] configure log collector 
    - [ ] configure the log driver for **all** container apps on new VM's 
  - [ ] setup ha proxy with ldcdb-1 and ldcdb-2 (requires replicated db to be ready)

- edit (x.146)
  - [ ] containerize symphony + edit app
  - [ ] plug in to github actions 
  - [ ] plublish container logs to log collector (x.153)
  - [ ] deploy on x.146 but proxy through x.153


