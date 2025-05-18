
# PowerShell Functions and Modules

PowerShell supports reusable code through functions and modules.

---

## 1. Functions

```powershell
function Get-Greeting {
    param ($name)
    "Hello, $name!"
}

Get-Greeting -name "Mohamed"
```

- Use `param()` to define parameters
- Functions return output by default

---

## 2. Script Blocks

```powershell
$block = { param($x) $x * 2 }
& $block 10
```

---

## 3. Modules

- Reusable libraries of functions and scripts
- Stored as `.psm1` files

```powershell
New-Item -ItemType Directory -Path "MyModule"
"function Get-Info { 'Module loaded' }" > .\MyModule\MyModule.psm1
Import-Module .\MyModule\MyModule.psm1
```

---

## 4. Discover and Use Modules

```powershell
Get-Module -ListAvailable
Install-Module -Name Az -Scope CurrentUser
```

Use `Export-ModuleMember` to control exports in your modules
