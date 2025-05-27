

### ✅ Fix: Enable Long Path Support in Windows

You can **easily fix** this by enabling Long Path support in Windows:

---

### 🔧 Step-by-step (for Windows 10/11 Pro & Home)

1. Press `Win + R`, type `gpedit.msc`, and press Enter

   > ❗ If you’re on Windows Home and `gpedit.msc` doesn’t work, skip to the **Registry Editor** method below.

2. Navigate to:

   ```
   Local Computer Policy > Computer Configuration > Administrative Templates > System > Filesystem
   ```

3. Find and double-click **"Enable Win32 long paths"**

4. Set it to **Enabled**, then click **OK**

5. Restart your PC to apply the changes

---

### 🛠 If you don’t have `gpedit.msc` (Windows Home)

1. Press `Win + R`, type `regedit`, and press Enter

2. Go to this registry key:

   ```
   HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem
   ```

3. On the right panel, find or **create a new DWORD (32-bit) Value** named:

   ```
   LongPathsEnabled
   ```

4. Double-click it and set the value to `1`

5. Restart your PC

---

### ✅ After Restarting:

Once you've enabled Long Path support and restarted:

1. Open PowerShell
2. Activate your virtual environment:

```powershell
.\venv\Scripts\Activate.ps1
```

3. Then try the install again:

```powershell
pip install -r requirements.txt
```


