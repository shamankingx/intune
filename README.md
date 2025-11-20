ADMX Repository

This repository stores Group Policy Administrative Templates (ADMX/ADML) for Windows, Microsoft 365, and third-party software.
It is designed for environments using:

Microsoft Intune (Custom ADMX Upload)

Active Directory Group Policy Central Store

Local Group Policy Editor (gpedit.msc)

📁 Repository Structure

Your structure (per vendor folder):

vendor-name/
    ├── admx/
    │     └── example.admx
    └── adml/
          └── example.adml


Full example structure:

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

Folder Rules

admx/ contains only .admx files

adml/ contains only .adml files, usually in a language subfolder (e.g., en-US/, th-TH/)

Each product or vendor has its own folder at the root level

📤 Uploading ADMX Files to Intune

Go to Intune Admin Center

Navigate to
Devices → Configuration → Import ADMX

Upload:

.admx files from vendor-name/admx/

.adml files from vendor-name/adml/ (include language folder)

Once uploaded, Intune will allow creating configuration profiles using these templates.

📚 Best Practices

Keep all vendors separated at the root level

Store ADMX and ADML files in their respective admx/ and adml/ folders

Use consistent commit messages, e.g.:

Update Chrome ADMX to version 131
Fix Citrix Workspace ADMX using FixMyADMX
Add custom ADMX for internal policy


Run FixMyADMX before uploading to Intune

Maintain a version history using a CHANGELOG.md

📄 License Notice

Some ADMX templates are copyrighted by their respective vendors.
Review vendor licensing conditions before redistribution.
