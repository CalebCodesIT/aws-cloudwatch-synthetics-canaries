Cloudformation templates must be deployed in order and are numbered in the directory: cf-templates

To deploy a cft,

```
cd cf-bin
./deploy <template-directory-name>
```

For example:

`./deploy 00-vpc`

Will deploy this template:
    `cf-templates/00-vpc/template.yml`

Additionally, in the `cf-bin` directory, a private file, not to be checked in can be created:

`set-stack-dir`

There is a template file for this that can be copied to .cf-bin/set-stack-dir

set the stack directory in this file and then you just have to type:

./deploy

it will source the set-stack-dir file and deploy the stack in the directory specified.

---
to deploy all templates at once

./deploy-all