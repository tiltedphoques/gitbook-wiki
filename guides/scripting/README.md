# Scripting

The ST server provides a set of scripting functions that you can use to customize and extend its functionality. To get started with scripting, create a subfolder in the server's "/resources/" directory with the name of your resource. Within that folder, create a "something.manifest" file that includes the following components:

```
[Resource]
name = "Example Resource"
version = 1.0.0
apiset = 1.0.0
description = "Official skyrim together example resource"
keywords = ["example", "resource"]
license = "MIT"
repository = ""
homepage = "https://skyrim-together.com/"
entrypoint = "main.lua"
```

Once you have created the manifest file, you can place your script file in the same folder. It's important to note that the main script file must have the same name as the "entrypoint" property in the script manifest. With these files in place, your script will be loaded by the ST server and its functionality will be available for use.
