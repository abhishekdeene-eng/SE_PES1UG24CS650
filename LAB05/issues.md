# Lab 05 – Static Code Analysis Issue Table

**Name:** Abhishek  
**SRN:** PES1UG24CS650  
**Repository:** L5_41_library_catalog_system

| Sl. No. | Tool | Issue identified in original code | Fix applied | Final result |
|---:|---|---|---|---|
| 1 | Pylint | Function naming and documentation problems | Used descriptive snake_case names and added docstrings | 10.00/10 |
| 2 | Pylint | Mutable default argument in `issue_book` | Changed the default to `None` and initialized the list inside the function | Resolved |
| 3 | Pylint | Unused variables and imports | Removed unused code and imports | Resolved |
| 4 | Bandit | Weak MD5 hashing | Replaced MD5 with SHA-256 | No issues identified |
| 5 | Bandit | Insecure random PIN generation | Used the `secrets` module | No issues identified |
| 6 | Bandit | Unsafe dynamic evaluation | Removed `eval` and used safer handling | No issues identified |
| 7 | Bandit | Shell command execution risk | Removed unsafe shell execution | No issues identified |
| 8 | Python quality | File handling without a context manager and encoding | Used `Path.open()` with a context manager and UTF-8 encoding | Resolved |
| 9 | Flake8 | Formatting and style violations | Corrected formatting and style | No errors |

## Final Verification

- Pylint score: 10.00/10
- Bandit: No issues identified
- Flake8: No errors reported

The original and final reports are saved separately as required.