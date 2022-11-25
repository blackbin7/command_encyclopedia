# Command Line Collections
---
## Table of Contents
- [Terminal](#terminal)
  - [Directory operations](#directory-operations)
  - [File operations](#file-operations)
  - [Selection operations](#selection-operations)
  - [Security operations](#security-operations)
  - [Program operations](#program-operations)
  - [Process operations](#process-operations)
  - [Time operations](#time-operations)
  - [Network operations](#network-operations)
  - [Other operations](#other-operations)
- [Markdown](#markdown)
- [Git](#git)



File operations
---------------
'mv' - Move a file or directory
 - 'mv file1 file2' - Rename file1 to file2
 - 'mv file1 file2 file3 dir1' - Move file1, file2, file3 to dir1. If dir1 does not exist, it will be created.

 - For error '-bash: /bin/mv: Argument list too long':
   - use 'xargs' to split the command into smaller chunks:
     - 'find . -name "*.txt" | xargs mv -t dir1'
   - use 'find -exec' to execute the command for each file:
     - 'find . -name "*.txt" -exec mv {} dir1 \;'


