# ovh-api-tool

## Mandatory config file for the api calls

Filename: ovh-api-tool.rc

Location: Next to the script
```
{
        "endpoint": "ovh-eu",
        "application_key": "<akey>",
        "application_secret": "<secret>",
        "consumer_key": "<ckey>"
}
```
# Usage

## Modus
```
usage: ovh-api-tool [-h] {read,write} ...

Read or alter dns objects via OVH api

positional arguments:
  {read,write}  mode
    read        Get object properties
    write       Alter object properties

optional arguments:
  -h, --help    show this help message and exit

```
## Read options
```
usage: ovh-api-tool read [-h] -z ZONE [-f FIELDTYPE] [-i RECORDID] [-p PROP]
                         [-v]

optional arguments:
  -h, --help            show this help message and exit
  -z ZONE, --zone ZONE  zoneName, e.g. domain.com
  -f FIELDTYPE, --fieldtype FIELDTYPE
                        fieldType, e.g. TLSA
  -i RECORDID, --recordid RECORDID
                        recordid
  -p PROP, --prop PROP  Property, e.g. target, fieldType, id, zone, ttl,
                        subDomain
  -v, --verbose         Verbose mode
```
## Write options
```
usage: ovh-api-tool write [-h] -z ZONE -i RECORDID -t TARGET

optional arguments:
  -h, --help            show this help message and exit
  -z ZONE, --zone ZONE  zoneName, e.g. domain.com
  -i RECORDID, --recordid RECORDID
                        recordid of record
  -t TARGET, --target TARGET
                        target of record
```

# tlsa-check
```
usage: tlsa-check [-h] -z ZONENAME -i RECORDID [-a] [-v]

Comparing saved/actual hash for one TLSA record

optional arguments:
  -h, --help            show this help message and exit
  -z ZONENAME, --zonename ZONENAME
                        zoneName, e.g. domain.com
  -i RECORDID, --recordid RECORDID
                        recordid
  -a, --autoupdate      Automatically update the record if missmatch
  -v, --verbose         Verbose output
```
