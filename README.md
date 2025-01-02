# Unreachable Code Warning in Julia

This repository demonstrates a scenario where Julia's unreachable code warning is not consistently triggered.  The example showcases a function with an `if-else` block that contains a `return` statement in every branch. Despite this, adding an extra `return` statement after the `if-else` block should trigger a warning, as that line is unreachable.  This highlights the compiler's limitations in detecting certain types of unreachable code.

## Bug Report

The issue is that the compiler might not detect the unreachable code, leading to potentially misleading code. Adding the extra `return 0` statement should produce an `unreachable code` warning.