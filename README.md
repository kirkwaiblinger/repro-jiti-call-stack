# repro-jiti-call-stack

## Requirements

- Windows
- Node (I'm using 23.10.0)

## Repro

0. `yarn install` (may need to `corepack enable`)

1. Run `yarn exec jiti stackTraceCJS.cts`.

    - This reports the TS file's path as `C:/path/to/repo/stackTraceCJS.cts`. 
    - Compare to `node stackTraceCJS.cts`, which reports the TS file's path as `C:\path\to\repo\stackTraceCJS.cts`.

2. Run `yarn exec jiti stackTraceESM.mts`.
    - This reports the TS file's path as `C:/path/to/repo/stackTraceESM.mts`.
    - Compare to `node stackTraceESM.mts`, which reports the TS file's path (in URL format) as `file:///C:/path/to/repo/stackTraceESM.mts`.
