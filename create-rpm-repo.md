### Sync and Publish a Repo

$> pulp-admin login -u admin    
$> pulp-admin rpm repo create --repo-id=foo     
$> pulp-admin rpm repo create --repo-id=zoo1 --relative-url=zoo1 --feed=http://repos.fedorapeople.org/repos/pulp/pulp/demo_repos/zoo/     
$> pulp-admin rpm repo sync run --repo-id=zoo1     
````
[wguo@dhcp-137-175 ~]$ pulp-admin rpm repo sync run --repo-id=zoo1
+----------------------------------------------------------------------+
                    Synchronizing Repository [zoo1]
+----------------------------------------------------------------------+

This command may be exited via ctrl+c without affecting the request.


Downloading metadata...
[/]
... completed

Downloading repository content...
[\]
[==================================================] 100%
RPMs:       0/0 items
Delta RPMs: 0/0 items

... completed

Downloading distribution files...
[==================================================] 100%
Distributions: 0/0 items
... completed

Importing errata...
[-]
... completed

Importing package groups/categories...
[-]
... completed

Cleaning duplicate packages...
[-]
... completed


Task Succeeded



Initializing repo metadata
[-]
... completed

Publishing Distribution files
[-]
... completed

Publishing RPMs
[==================================================] 100%
32 of 32 items
... completed

Publishing Delta RPMs
... skipped

Publishing Errata
[==================================================] 100%
4 of 4 items
... completed

Publishing Comps file
[==================================================] 100%
3 of 3 items
... completed

Publishing Metadata.
[-]
... completed

Closing repo metadata
[-]
... completed

Generating sqlite files
... skipped

Generating HTML files
... skipped

Publishing files to web
[-]
... completed

Writing Listings File
[-]
... completed


Task Succeeded
````

https://<domain>/pulp/repos/zoo1/
