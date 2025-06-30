# Change Log

All notable changes to the "scl" extension will be documented in this file.

## [Latest] - 2025-06-27

### Added - Development Environment

- **Dev Container Support**: Complete development container configuration for VS Code extension development
  - Pre-configured Node.js 18 environment with TypeScript support
  - Automated installation of VS Code extension development tools (`@vscode/vsce`, `yo`, `generator-code`)
  - Git and GitHub CLI integration for version control
  - Optimized VS Code settings for extension development

### Added - Syntax Highlighting Enhancements

- **Extended Keywords Support**:
  - Program blocks: `PROGRAM`, `END_PROGRAM`, `ORGANIZATION_BLOCK`, `OB`, `END_OB`
  - Exception handling: `TRY`, `CATCH`, `THROW`, `FINALLY`, `END_TRY`
  - Declaration modifiers: `RETAIN`, `NON_RETAIN`, `CONSTANT`, `PERSISTENT`
  - Access modifiers: `READ_ONLY`, `NO_CHECK`, `KNOW_HOW_PROTECT`
  - Compiler directives: `TITLE`, `AUTHOR`, `FAMILY`, `NAME`, `VERSION`

- **Enhanced Data Types**:
  - S7-1500 specific types: `LWORD`, `WCHAR`, `LTIME`, `LDT`, `LTOD`
  - IEC standard types: `IEC_COUNTER`, `IEC_LTIMER`
  - System types: `DB_ANY`, `HW_ANY`, `PORT`, `RTM`, `BLOCK_FB`, `BLOCK_FC`, `BLOCK_DB`, `BLOCK_SDB`

- **Comprehensive Built-in Functions**:
  - Mathematical functions: `ATAN2`, `DEGREES`, `RADIANS`, `FRAC`, `EXPT`
  - Arithmetic operations: `ADD`, `SUB`, `MUL`, `DIV`, `NORM_X`, `SCALE_X`
  - IEC Timers/Counters: `TON`, `TOF`, `TP`, `CTU`, `CTD`, `CTUD`, `R_TRIG`, `F_TRIG`
  - String manipulation: `LEN`, `CONCAT`, `LEFT`, `RIGHT`, `MID`, `INSERT`, `DELETE`, `REPLACE`, `FIND`
  - System functions: `GET_ERROR_ID`, `IS_NULL`, `IS_ARRAY`, `SIZEOF`, `TYPEINFO`
  - Communication functions: `ALARM`, `ALARM_8`, `ALARM_8P`, `NOTIFY`, `AR_SEND`, `AR_RECV`
  - Time functions: `RD_SYS_T`, `WR_SYS_T`, `SET_TIMEZONE`, `RTM`, `RUNTIME`

- **Compiler Pragmas and Attributes**:
  - Pragma syntax highlighting: `{pragma_name := 'value'}`
  - S7-1500 pragmas: `S7ServerActive`, `SetOKFlag`, `MonitorArrayLimits`, `OverwriteBlocks`, etc.
  - System attributes: All `S7_*` attributes with proper highlighting
  - Interface attributes: `ExternalAccessible`, `ExternalVisible`, `ExternalWritable`

- **Enhanced Constants and Literals**:
  - Improved number format support including exponential notation
  - Octal number support: `8#777`
  - System constants: `PI`, `E`, `TRUE`, `FALSE`, `NULL`
  - Status constants: `OK`, `ERROR`, `BUSY`, `DONE`, `WARNING`
  - Data type limits: `INT_MIN`, `INT_MAX`, `DINT_MIN`, `DINT_MAX`, etc.

- **Advanced String Support**:
  - WSTRING support with double-quoted syntax: `"text"`
  - Enhanced escape sequences: `$$`, `$'`, `$L`, `$N`, `$P`, `$R`, `$T`
  - Better string pattern recognition

### Added - Code Snippets (68 New Snippets)

- **Block Templates**:
  - Data Block template (`db`)
  - User Data Type template (`udt`)
  - Function with error handling template (`fnerr`)

- **IEC Standard Components**:
  - Timer snippets: TON (`timer`), TOF (`tof`), TP (`tp`)
  - Counter snippets: CTU (`ctu`), CTD (`ctd`), CTUD (`ctud`)
  - Edge detection: Rising edge (`re`), Falling edge (`fe`)

- **Error Handling Patterns**:
  - Standard error handling template (`error`)
  - Input validation patterns
  - Status code management

- **Mathematical and Control Functions**:
  - Basic arithmetic: `add`, `sub`, `mul`, `div`
  - Advanced math: `abs`, `sqrt`, `exp`, `ln`, `sin`, `cos`, `tan`
  - Control functions: `limit`, `min`, `max`, `sel`, `mux`
  - PID controller setup (`pid`)
  - Analog scaling (`scale`)

- **String Operations**:
  - String manipulation: `strlen`, `strcat`, `strleft`, `strright`, `strmid`

- **Bit Operations**:
  - Bitwise operations: `bitand`, `bitor`, `bitxor`, `bitnot`
  - Shift operations: `shl`, `shr`

- **Code Documentation Templates**:
  - Safety-critical code comments (`safety`)
  - Performance consideration notes (`performance`)
  - TODO tracking (`todo`)
  - Bug tracking (`fixme`)

### Improved

- Better recognition of hardware module types: `CPU`, `IM`, `CM`, `CP`, `FM`, `SM`, `AI`, `AO`, `DI`, `DO`
- Enhanced block type recognition: `SFC`, `SFB`, `FC`, `FB`, `DB`, `UDT`, `VAT`
- Improved HMI function pattern matching: `HMI_*`, `OS_*`, `GRAPH_*`, `BATCH_*`

## [0.2.1]

- Added DTL and ENO to datatypes
- Added highlighting of some more key words
- Added highlighting of some functions
- Added highlighting of null

## [0.2.0]

Mostly additions from Sikilde

- Added support for escaping strings with both `$` and `\`
- Fixed function block support
- Added data_block support
- Added datatypes ton_time, tof_time, tp_time and iec_timer
- Added recognition of local variables starting with `#`
- Added recognition of variable in declaration
- Added .db file extension support

## [0.1.1]

- Reverted "fix for a bug where escaped single quote in string broke the string highlighting"

## [0.1.0]

- Merged sikilde's fix for a bug where escaped single quote in string broke the string highlighting
- Merged sikilde's multi language comment block pattern
- Merged jbradshaw14's fix for timers and local variables
- Added TcPOU and TcGVL (TwinCAT) file extensions to allow for syntax highlighting of the ST in the files (does not support the xml-wrapper)
- Added updates to readme

## [0.0.21]

- Merged highlighting fix of region names

## [0.0.20]

- Added missing system attributes

## [0.0.19]

- Merged pull requests with snippets for more conversions
- Merged pull requests with snippets for region

## [0.0.10]

- Bugfix wstring_to_sint

## [0.0.9]

- wstring conversions added (by d-ani)

## [0.0.8]

- Added Class A conversions to snippets and highlighting

## [0.0.7]

- Fixed version number discrepancy between changelog and actual version number

## [0.0.6]

- Reduced complexity of how functions are recognized
- Fixed a bug where function names would be tokenized as function type

## [0.0.5]

- This version was skipped (the version number was altered before publish)

## [0.0.4]

- Added icon

## [0.0.3]

- Added snippets for type conversion
- Edited highlighting of quoted function calls (ignore whitespace)

## [0.0.2]

- Added uint to syntax
- Edited regex for recognizing time constants
- Added indent patterns
- Block comment can now be applied by pressing **Shift+Alt+A**

## [0.0.1]

- Initial release

## [0.2.0]
Mostly additions from Sikilde
- Added support for escaping strings with both `$` and `\`
- Fixed function block support
- Added data_block support
- Added datatypes ton_time, tof_time, tp_time and iec_timer
- Added recognition of local variables starting with `#`
- Added recognition of variable in declaration 
- Added .db file extension support

## [0.1.1]
- Reverted "fix for a bug where escaped singel qoute in string broke the string highlighting"

## [0.1.0]
- Merged sikilde's fix for a bug where escaped singel qoute in string broke the string highlighting
- Merged sikilde's milty language comment block pattern
- Merged jbradshaw14's fix for timers and local variables
- Added TcPOU and TcGVL (TwinCAT) file extensions to allow for syntax highlighting of the ST in the files (does not support the xml-wrapper)
- Added updates to readme

## [0.0.21]
- Merged highlighting fix of region names

## [0.0.20]
- Added missing system attributes

## [0.0.19]
- Merged pull requests with snippets for more conversions
- Merged pull requests with snippets for region

## [0.0.10]
- Bugfix wstring_to_sint

## [0.0.9]
- wstring conversions added (by d-ani)

## [0.0.8]
- Added Class A conversions to snippets and highlighting

## [0.0.7]
- Fixed version number discrepancy between changelog and actual version number

## [0.0.6]
- Reduced complexity of how functions are recognized
- Fixed a bug where function names would be tokenized as function type

## [0.0.5]
- This version was skipped (the version number was altered before publish)

## [0.0.4]
- Added icon

## [0.0.3]
- Added snippets for type conversion
- Edited highlighting of quoted function calls (ignore whitespace)

## [0.0.2]
- Added uint to syntax
- Edited regex for recognizing time constants
- Added indent patterns
- Block comment can now be applied by pressing <kbd>Shift</kbd>+<kbd>Alt</kbd>+<kbd>A</kbd>

## [0.0.1]
- Initial release