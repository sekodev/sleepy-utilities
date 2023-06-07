# Sleepy Utilities

A general purpose library that you can use in Solar2D projects with minimal modification.

## Usage instructions
**Import library**
```sh
local utils = require "utils"
```

**Create slider widget**
```sh
utils.createSliderControl(targetGroup, optionsSliderControl)
```

**Close databases**
```sh
tableDatabases = utils.closeDatabases(tableDatabases)
```

**Close files**
```sh
tableFiles = utils.closeDatabases(tableFiles)
```

**Resume timers**
```sh
utils.resumeTimers(tableTimers)
```

**Pause timers**
```sh
utils.pauseTimers(tableTimers)
```

**Cancel timers**
```sh
tableTimers = utils.cancelTimers(tableTimers)
```

**Clear display group**
```sh
utils.clearDisplayGroup(targetGroup)
```

**Clear table**
```sh
targetTable = utils.clearTable(targetTable)
```
