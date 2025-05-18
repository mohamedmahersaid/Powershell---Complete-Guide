
# PowerShell Syntax and Variables

Understanding PowerShell syntax and variable usage is key to writing efficient scripts.

---

## 1. Basic Syntax

```powershell
Write-Output "Hello, PowerShell"
Get-Service
$process = Get-Process
```

- Cmdlets use `Verb-Noun` naming
- Use `|` (pipe) to pass objects

---

## 2. Variables

```powershell
$name = "Admin"
$number = 5
$items = @(1, 2, 3)
```

- Variables begin with `$`
- Arrays use `@()`, Hashtables use `@{}`

---

## 3. Data Types

```powershell
[int]$id = 123
[string]$city = "New York"
[datetime]$now = Get-Date
```

Use `Get-Member` to inspect types:
```powershell
$city | Get-Member
```

---

## 4. String Interpolation

```powershell
$name = "User"
Write-Output "Welcome, $name!"
```

Use `"double quotes"` for interpolation, `'single quotes'` for literal
