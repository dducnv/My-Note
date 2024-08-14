# convert all file names in a folder from lowercase to uppercase
## for first letter

```powershell
Get-ChildItem -File | ForEach-Object {
    $newName = $_.Name.Substring(0,1).ToUpper() + $_.Name.Substring(1)
    Rename-Item $_.FullName -NewName $newName
}
```

## for all
```powershell
Get-ChildItem | Rename-Item -NewName { $_.Basename.ToUpper() + $_.Extension }
```
