---
title: Netlify CLI functions command
description: Run netlify dev locally
---

# `functions`

<!-- AUTO-GENERATED-CONTENT:START (GENERATE_COMMANDS_DOCS) -->
Manage netlify functions
The `functions` command will help you manage the functions in this site


**Usage**

```bash
netlify functions
```

| Subcommand | description  |
|:--------------------------- |:-----|
| [`functions:build`](/commands/functions#functionsbuild) | Build functions locally  |
| [`functions:create`](/commands/functions#functionscreate) | Create a new function locally  |
| [`functions:invoke`](/commands/functions#functionsinvoke) | Trigger a function while in netlify dev with simulated data, good for testing function calls including Netlify's Event Triggered Functions  |


**Examples**

```bash
netlify functions:create --name function-xyz
netlify functions:build --name function-abc --timeout 30s
```

---
## `functions:build`

Build functions locally


**Usage**

```bash
netlify functions:build
```

**Flags**

- `functions` (*option*) - Specify a functions folder to build to
- `src` (*option*) - Specify the source folder for the functions

---
## `functions:create`

Create a new function locally

**Usage**

```bash
netlify functions:create
```

**Arguments**

- name - name of your new function file inside your functions folder

**Flags**

- `name` (*option*) - function name
- `url` (*option*) - pull template from URL

**Examples**

```bash
netlify functions:create
netlify functions:create hello-world
netlify functions:create --name hello-world
```

---
## `functions:invoke`

Trigger a function while in netlify dev with simulated data, good for testing function calls including Netlify's Event Triggered Functions

**Usage**

```bash
netlify functions:invoke
```

**Arguments**

- name - function name to invoke

**Flags**

- `name` (*option*) - function name to invoke
- `functions` (*option*) - Specify a functions folder to parse, overriding netlify.toml
- `querystring` (*option*) - Querystring to add to your function invocation
- `payload` (*option*) - Supply POST payload in stringified json, or a path to a json file
- `identity` (*boolean*) - simulate Netlify Identity authentication JWT. pass --no-identity to affirm unauthenticated request

**Examples**

```bash
$ netlify functions:invoke
$ netlify functions:invoke myfunction
$ netlify functions:invoke --name myfunction
$ netlify functions:invoke --name myfunction --identity
$ netlify functions:invoke --name myfunction --no-identity
$ netlify functions:invoke myfunction --payload "{"foo": 1}"
$ netlify functions:invoke myfunction --querystring "foo=1
$ netlify functions:invoke myfunction --payload "./pathTo.json"
```

---

<!-- AUTO-GENERATED-CONTENT:END -->
