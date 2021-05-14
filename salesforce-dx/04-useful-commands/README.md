# SFDX Useful Commands

### Get Org details

```bash
$ sfdx force:org:display -u yourOrgAlias
```

<br>

### Deploy Metadata

In order to push a metadata from an unconnected/new source to an org we can use the `deploy` command:

```bash
$ sfdx force:source:deploy -p "/PATH/TO/YOUR/COMPONENT"
```

<br>

### Retrieve Metadata

To retrieve metadata from scratch org to any destination in local computer, or the component doesn't exist in the local we can use the `retrieve` command:

```bash
$ sfdx force:source:retrieve -p "/PATH/TO/YOUR/COMPONENT"
$ sfdx force:source:retrieve -m "ApexClass:YOURAPEXCLASS"
$ sfdx force:source:retrieve -m Flow:yourflowName -u sourceorg
```

Note that the name of the metadata is the API Name, not the filename. To get all files of a
certain metadata type:

```bash
$ sfdx force:source:retrieve -m LightningComponentBundle
$ sfdx force:source:retrieve -m PermissionSet:My_Perm_Set
```

<br>

### Alias

To set an Alias for an existing org we use this command:

```bash
$ sfdx force:alias:set My_Alias_Name=user@namespace.com.sc
```