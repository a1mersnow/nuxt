---
title: "nuxi build"
description: "Build your Nuxt application."
links:
  - label: Source
    icon: i-simple-icons-github
    to: https://github.com/nuxt/cli/blob/main/src/commands/build.ts
    size: xs
---

```bash [Terminal]
npx nuxi build [--prerender] [--preset] [--dotenv] [--log-level] [rootDir]
```

The `build` command creates a `.output` directory with all your application, server and dependencies ready for production.

Option        | Default          | Description
-------------------------|-----------------|------------------
`rootDir` | `.` | The root directory of the application to bundle.
`--prerender` | `false` | Pre-render every route of your application. (**note:** This is an experimental flag. The behavior might be changed.)
`--preset` | - | Set a [Nitro preset](https://nitro.unjs.io/deploy#changing-the-deployment-preset)
`--dotenv` | `.` | Point to another `.env` file to load, **relative** to the root directory.
`--log-level` | `info` | Specify build-time logging level, allowing `silent` \| `info` \| `verbose`.

::note
This command sets `process.env.NODE_ENV` to `production`.
::

::note
`--prerender` will always set the `preset` to `static`
::
