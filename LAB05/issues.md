# Lab 5: Static Code Analysis — Issue Table

**Name:** Abhishek  
**SRN:** PES1UG24CS650  
**Program:** Library Catalog System

| Issue | Type | Line(s) | Description | Fix Approach |
|---|---|---|---|---|
| Unsafe `eval()` usage | Security (Medium) | 42 | Evaluating a supplied expression can allow arbitrary code execution. | Replaced `eval()` with a direct fine calculation using a daily rate. |
| Weak MD5 hashing | Security (High) | 47 | MD5 is not appropriate for security-sensitive hashing. | Replaced MD5 with SHA-256. |
| Shell command execution | Security (High) | 58 | `os.system()` executes a shell command and may introduce command-injection risks. | Removed shell execution and used a Python `print()` statement. |
| Insecure random PIN generation | Security (Low) | 51 | `random.randint()` is not designed for security-sensitive PIN generation. | Replaced it with `secrets.randbelow()`. |
| Bare exception handling | Code Quality | 26 | A bare `except:` can hide unexpected errors. | Removed the broad exception handler and checked whether the book exists. |
| Mutable default argument | Code Quality | 12 | `active_issues=[]` can share a mutable list across function calls. | Changed the default to `None` and initialized the list inside the function. |
| Hardcoded access key | Security | 62 | A fixed librarian key was embedded in the source code and printed. | Removed the hardcoded key and its print statement. |
| Unused import | Code Quality / Style | 6 | The `csv` module was imported but never used. | Removed the unused import. |
| Unused variable | Code Quality / Style | 31 | The `late_fee` variable was assigned but never used. | Removed the unused variable. |
| Comparison with `None` | Style | 32 | The code used `== None`. | Replaced it with a direct dictionary membership check. |
| Missing final newline | Formatting | 73 | The original file did not end with a newline. | Added a final newline. |

**Note:** Line numbers refer to the original program before corrections. Severity labels are included where they correspond to the original Bandit findings; other findings are categorized by issue type.