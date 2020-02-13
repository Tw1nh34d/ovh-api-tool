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
usage: ovh-api-tool read [-h] -z ZONE -f FIELDTYPE

optional arguments:
  -h, --help            show this help message and exit
  -z ZONE, --zone ZONE  zoneName, e.g. domain.com
  -f FIELDTYPE, --fieldtype FIELDTYPE
                        fieldType, e.g. TLSA
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
