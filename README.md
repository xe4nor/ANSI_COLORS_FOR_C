# ANSI_COLORS_FOR_C

# 🎨 ANSI Colors for C

Bring color to your C programs.  
This header gives you full access to **ANSI escape sequences** for colorful and styled terminal output – clean, portable, and ready to use.




## ✨ Features

- ✅ Full **foreground** and **background** color support  
- 🌈 Bright color variants for *neon vibes*  
- 💪 Formatting like **bold**, _underline_, and even `hidden`  
- 🔌 Just `#include "ansi_colors.h"` and you're ready




## 🎯 Ideal For

- Debugging output in color  
- Linux / WSL / macOS terminals  
- Windows (with VT100 enabled – see tip below)



## 🚀 Quick Example


```c
#include "ansi_colors.h"

printf(ANSI_GREEN "✓ Success!\n" ANSI_RESET);
printf(ANSI_RED ANSI_BOLD "✗ Error!\n" ANSI_RESET);
```

## 🪛 Windows VT100 Support To enable ANSI colors on cmd.exe or PowerShell:

```c
#include <windows.h>

void EnableVTMode() {
    DWORD mode = 0;
    HANDLE hOut = GetStdHandle(STD_OUTPUT_HANDLE);
    GetConsoleMode(hOut, &mode);
    SetConsoleMode(hOut, mode | ENABLE_VIRTUAL_TERMINAL_PROCESSING);
}
```


