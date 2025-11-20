# ADMX Repository

This repository stores **Group Policy Administrative Templates (ADMX/ADML)** for Windows, Microsoft 365, and third-party applications.  
It is designed to support:

- Microsoft Intune (Custom ADMX Import)
- Active Directory Group Policy (Central Store)
- Local Group Policy Editor (gpedit.msc)

---

## 📁 Repository Structure

Each vendor or product folder contains two subfolders:


Each vendor or product folder contains two subfolders:

```
vendor-name/
    ├── admx/
    │     └── example.admx
    └── adml/
          └── example.adml
```

Full example:

```
├── microsoft/
│     ├── admx/
│     └── adml/
├── chrome/
│     ├── admx/
│     └── adml/
├── firefox/
│     ├── admx/
│     └── adml/
├── citrix/
│     ├── admx/
│     └── adml/
└── custom/
      ├── admx/
      └── adml/
```


**Rules:**

- `admx/` folder contains only `.admx` files  
- `adml/` folder contains only `.adml` files (often inside `en-US/`, `th-TH/`, etc.)  
- Each product or vendor is stored in a separate root folder  

---

📤 Uploading ADMX Files to Microsoft Intune

Go to Intune Admin Center

Navigate to
Devices → Configuration → Import ADMX

Upload:

.admx files from vendor-name/admx/

.adml files from vendor-name/adml/ (include language subfolder if required)

After uploading, you can create a configuration profile using the imported template.

📚 Best Practices

Keep vendors separated at the root level

Maintain consistent folder structure (admx/ and adml/)

Recommended commit examples:

Update Chrome ADMX to version 131
Fix Citrix Workspace ADMX using FixMyADMX
Add custom internal ADMX template


Always validate or fix templates before uploading to Intune

Consider maintaining a CHANGELOG.md for tracking versions

📄 Licensing Notice

Some ADMX/ADML templates are copyrighted by their respective software vendors.
Please review and comply with vendor licensing terms before redistributing files.
