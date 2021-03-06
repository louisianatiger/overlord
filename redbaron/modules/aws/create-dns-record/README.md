# create-dns-record

Adds records to a domain using AWS Route53

# Arguments

| Name                      | Value Type | Description
|---------------------------| ---------- | -----------
|`type`                     | String     | The record type to add. Valid values are A, AAAA, CAA, CNAME, MX, NAPTR, NS, PTR, SOA, SPF, SRV and TXT.
|`name`                     | String     | Use @ to create the record at the root of the domain or enter a hostname to create it elsewhere. A records are for IPv4 addresses only and tell a request where your domain should direct to.
|`counter`                  | Integer    | Number of records to add. Default value is 1
|`ttl`                      | Integer    | The TTL of the record(s). Default value is 300
|`records`                  | Map(any)   | A map of records to add. Domains as keys and IPs as values.
|`zone`                     | String     | AWS ZoneID of the Route53 for that domain

# Outputs

| Name                      | Value Type | Description
|---------------------------| ---------- | -----------
|`records`                  | Map(any)   | Map containing the records added to the domain. Domains as keys and IPs as values.

