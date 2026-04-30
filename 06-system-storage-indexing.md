# DocuWare Knowledge Center - System Requirements, File Cabinets, Storage & Indexing

---

## DocuWare Version 7.13 On-Premises System Requirements

### DocuWare Server Setup
- Local administrator rights needed for installation
- .NET Framework version 4.8
- .NET version 8
- Windows Installer 4.5

### DocuWare Client Setup
- Administrator privileges required for new Desktop Apps installations (not needed for updates)
- .NET Framework 4.8, when installing the Windows Explorer client .NET 8
- Windows Installer 4.5

### Operating Systems for Server and Clients
Supported platforms:
- Windows Server 2025 (x64)
- Windows Server 2022 (x64)
- Windows Server 2019 (x64)
- Windows Server 2016 (x64)
- Windows 11 (x64)
- Windows 10 (x86 + x64), version H2

**Restrictions:** Windows 11/10 are NOT recommended because of strong IIS request limits (10 concurrent requests maximum). Home editions unsuitable for servers. AWS unsupported. Terminal servers and domain controllers are not supported for DocuWare Server installations.

Support aligns with Microsoft's official OS support lifecycle.

### Browsers for Web Applications
Supported: Firefox, Chrome, Edge

### Databases
- Microsoft SQL Server 2016, 2017, 2019 and 2022 [Collation Latin1_General_CI_AS]
- MySQL 8 [Legacy basic authentication; Collation utf8mb3_unicode_ci], version 8.0.28

### SMTP Server
DocuWare needs an external SMTP server to send notification emails, e.g. when users want to reset their password.

### Special Requirements

**DocuWare Desktop:** Desktop Experience required on Windows Server installations.

**Outlook Integration:** Microsoft Office 2016, 2019 und 2021, each in 32-bit and 64-bit versions, and Microsoft Office 365. Plus Microsoft Exchange Server 2016, 2019.

**Mail Connection:** Microsoft Exchange Server 2016, 2019 and Microsoft Office 365.

**Outlook Web App:** Microsoft Office 365.

**DocuWare Request:** .NET Framework 4.5 or higher is required.

**DocuWare Export:** Microsoft .NET Desktop Runtime version 8 (x86) is required.

**Electronic Signatures:** ValidatedID provider supports specific devices for biometric signatures.

**Intelligent Indexing (Local Installation):**
- Windows Server 2019 (Standard or Datacenter Edition, not within VMWare)
- 4 Processor cores
- 8 GB RAM
- Optional SQL Server 2019/2022
- Requires Mirantis Container Runtime with licensing

### Encryption
Since DocuWare version 7.6, the use of SSL/TLS for the encryption of HTTP traffic is mandatory.

### Hardware Requirements

**DocuWare Services:**
- CPU: 2 × 2.0 GHz minimum, 4 × 3.2 GHz recommended
- RAM: 4 GB minimum, 8 GB recommended
- Storage: minimum 5 GB hard disk space, SSD recommended; separate drives for documents

**Database (Internal):**
- CPU: minimum 2 × 1.4 GHz, recommended 2 × 3.2 GHz
- RAM: minimum 1 GB
- Storage: minimum 20 GB

For systems exceeding 1 Million documents (without fulltext index) or with more than 200,000 document pages, SQL Server recommended. MySQL 32-bit not recommended with Workflow Manager. Dedicated machine recommended for larger installations.

**Fulltext Service:**
- CPU: minimum 1 × 1.4 GHz, recommended 2 × 3.2 GHz
- RAM: minimum 1 GB, recommended 2 GB
- Dedicated machine recommended for larger installations

**Example Configurations:**

*All components on one machine without Fulltext (Internal DB):*
- Minimal: CPU 4 × 2.0 GHz; RAM 5 GB
- Recommended: CPU 6 × 3.2 GHz; RAM 9 GB

*With SQL Server and Fulltext:*
- Minimal: CPU 5 × 2.0 GHz; RAM 6 GB
- Recommended: CPU 8 × 3.2 GHz; RAM 14 GB

**Desktop Apps (Scan & Import Clients):**
- CPU: 4 × 2.0 GHz minimum
- RAM: 4 GB minimum, 8 GB recommended
- Storage: minimum 2 GB hard disk space for programs

Supported version: DocuWare on-premises 7.13

---

## DocuWare Version 7.12 On-Premises System Requirements

### Server Setup
- Local administrator rights on the computer
- .NET Framework version 4.8
- .NET version 8
- Windows Installer 4.5

### Client Setup
- Administrator privileges for new installations only
- .NET Framework 4.8, Windows Explorer client needs .NET 8
- Windows Installer 4.5

### Supported Operating Systems
Windows 10 (x86 + x64) version H2, Windows 11 (x64), Windows Server 2016/2019/2022/2025 (all x64).

NOT recommended due to IIS request limits (10 concurrent requests max). AWS unsupported. Terminal servers and domain controllers prohibited.

### Browser Compatibility
Firefox, Chrome, Edge

### Database Options
- Microsoft SQL Server 2016, 2017, 2019 and 2022 [Collation Latin1_General_CI_AS]
- MySQL 8 [Legacy basic authentication; Collation utf8mb3_unicode_ci], version 8.0.28

### Encryption
SSL/TLS mandatory since version 7.6.

### Hardware Specifications

**DocuWare Services:** CPU 2 × 2.0 GHz min / 4 × 3.2 GHz rec; RAM 4 GB min / 8 GB rec; Storage min 5 GB, SSD recommended.

**Database (Internal):** CPU min 2 × 1.4 GHz; RAM min 1 GB; Disk min 20 GB.

**Fulltext Service:** CPU min 1 × 1.4 GHz / 2 × 3.2 GHz rec; RAM min 1 GB / 2 GB rec.

### Special Features
- Outlook Integration: Microsoft Office 2016, 2019, 2021 + Exchange Server 2016, 2019
- Electronic Signatures: ValidatedID biometric devices
- Intelligent Indexing: Windows Server 2019, 4 cores, 8 GB RAM, Mirantis Container Runtime
- SMTP server mandatory for notifications
- Desktop Experience required on Windows Server
- DocuWare Request needs .NET Framework 4.5+

---

## DocuWare Version 7.11 On-Premises System Requirements

### Server Setup
- Local administrator rights, .NET Framework 4.8, .NET 8, Windows Installer 4.5

### Client Setup
- Admin rights for new installs only, .NET Framework 4.8 (Windows Explorer client: .NET 8), Windows Installer 4.5

### Operating Systems
Windows 10 (x86 + x64) version H2, Windows 11 (x64), Windows Server 2016/2019/2022 (all x64).

IIS request limits make Windows 10 NOT recommended. AWS, terminal servers, domain controllers unsupported.

### Browsers
Firefox, Chrome, Edge

### Database Support
- Microsoft SQL Server 2016, 2017, 2019 and 2022
- MySQL 5.6 - 5.7
- MySQL 8 (version 8.0.28)

### Special Requirements
- Desktop Experience for DocuWare Desktop on Windows Server
- Connect to Outlook: Microsoft Office 2016, 2019, 2021 or Office 365
- Intelligent Indexing: Windows Server 2019, 4 cores, 8 GB RAM, Mirantis Container Runtime
- SSL/TLS mandatory since v7.6

### Hardware
- DocuWare Services: CPU 2 × 2.0 GHz min / 4 × 3.2 GHz rec; RAM 4 GB min / 8 GB rec; Disk min 5 GB, SSD recommended
- Database: min 2 × 1.4 GHz, 1 GB RAM, 20 GB disk
- Fulltext: min 1 × 1.4 GHz, 1 GB RAM
- Desktop Apps: CPU 4 × 2.0 GHz min; RAM 4 GB min / 8 GB rec

---

## DocuWare Version 7.10 On-Premises System Requirements

### Server Setup
Local admin rights, .NET Framework 4.8, .NET 8, Windows Installer 4.5

### Client Setup
Admin rights for new installations. .NET Framework 4.8, Windows Explorer client .NET 8, Windows Installer 4.5

### Operating Systems
Windows 10 (x86 + x64), Windows 11 (x64), Windows Server 2016/2019/2022 (all x64).

Windows 10 not recommended (IIS 10 concurrent request limit). Home editions unsupported for servers. AWS, terminal servers, domain controllers unsupported.

### Browsers
Firefox, Chrome, Edge Chromium

### Databases
- Microsoft SQL Server 2016, 2017, 2019 and 2022
- MySQL 5.6 - 5.7
- MySQL 8 (version 8.0.28; later versions have .NET connectivity issues)

### Special Requirements
- Desktop Experience for DocuWare Desktop on Windows Server
- Outlook: Microsoft Office 2016, 2019, 2021 (32/64-bit) + Exchange Server 2016, 2019
- Mail: Exchange Server 2016, 2019
- Electronic Signatures: ValidatedID
- Intelligent Indexing: Windows Server 2019, 4 cores, 8 GB RAM, Mirantis Container Runtime
- SSL/TLS mandatory since v7.6

### Hardware
- DocuWare Services: CPU 2 × 2.0 GHz min; RAM 4 GB min; 5 GB disk
- Recommended: CPU 4 × 3.2 GHz; RAM 8 GB; SSD
- Internal DB: CPU 2 × 1.4 GHz min; RAM 1 GB; 20 GB disk
- Fulltext: CPU 1 × 1.4 GHz min; RAM 1 GB
- Desktop Apps: CPU 4 × 2.0 GHz; RAM 4 GB min; 2 GB disk

---

## DocuWare Version 7.9 On-Premises System Requirements

### Server Setup
Local admin rights, .NET Framework 4.8, .NET 6, Windows Installer 4.5

### Client Setup
Admin rights for new installations. .NET Framework 4.8, Windows Explorer client .NET 6, Windows Installer 4.5

### Operating Systems
Windows 10 (x86 + x64) version H2, Windows 11 (x64), Windows Server 2016/2019/2022 (x64).

Windows 10 not recommended (IIS limits). Home editions unsupported. AWS, terminal servers, domain controllers unsupported.

### Browsers
Firefox 50+, Chrome 54+, Edge Chromium

### Database Support
- Microsoft SQL Server 2012, 2014, 2016, 2017, 2019, 2022
- Oracle 12c, 18c, 19c (no longer supported for new installations; v7.9 is the last Oracle-supporting version)
- MySQL 5.6 - 5.7
- MySQL 8

### Special Requirements
- Desktop Experience on Windows Server
- Connect to Outlook: Microsoft Office 2013, 2016, 2019 + Microsoft 365 + Exchange Server 2010, 2013, 2016, 2019
- DocuWare Request: .NET Framework 4.5+
- Electronic Signatures: ValidatedID
- Intelligent Indexing: Windows Server 2019, 4 cores, 8 GB RAM, Mirantis Container Runtime + optional SQL Server 2019/2022
- SSL/TLS mandatory since v7.6

### Hardware
- DocuWare Services: CPU 2 × 2.0 GHz min / 4 × 3.2 GHz rec; RAM 4 GB min / 8 GB rec; 5 GB disk, SSD rec
- Internal DB: CPU 2 × 1.4 GHz min / 2 × 3.2 GHz rec; RAM 1 GB; 20 GB disk
- Fulltext: CPU 1 × 1.4 GHz min / 2 × 3.2 GHz rec; RAM 1 GB min / 2 GB rec
- Desktop Apps: CPU 4 × 2.0 GHz; RAM 4 GB min / 8 GB rec; 2 GB disk

---

## System Requirements DocuWare Cloud

### General Requirements

**Operating Systems:**
Windows Server 2025/2022/2019/2016 (x64), Windows 11 (x64), Windows 10 (x86+x64) version H2.

Microsoft's end-of-support timelines dictate when DocuWare discontinues version support simultaneously.

**Browser Compatibility:**
Firefox, Chrome, Edge. Provider support expiration triggers automatic DocuWare discontinuation.

**Desktop Client Setup:**
- Initial installations require local administrator privileges; updates don't
- .NET Framework 4.8, Windows Explorer client or Local Data Connector needs .NET 8
- Windows Installer 4.5

**Data Transfer Security:**
Access only via TLS protocol version 1.2 with cipher suites: TLS_AES_128_GCM_SHA256, TLS_AES_256_GCM_SHA384, and ECDHE variants.

### Special Requirements
- DocuWare Desktop: Desktop Experience on Windows Server; min 4 × 2.0 GHz CPU, 4 GB RAM (8 GB rec)
- Outlook: Microsoft Office 2016, 2019, 2021 (32/64-bit) and Office 365; Exchange Server 2016, 2019
- Mail: Exchange Server 2016, 2019, Office 365
- Outlook Web App: Office 365 only
- Request: .NET Framework 4.5+
- Export: Microsoft .NET Desktop Runtime version 8 (x86)
- Electronic Signatures: ValidatedID biometric devices

### Limitations
- Document viewing capped at 2 GB
- Workflows limited to 5000 events per instance
- Autoindex minimum interval: 10 minutes

---

## File Cabinets - Introduction

File cabinets can be created with just a few clicks. Pre-defined components including fields use modular principles for constructing store and search dialogs, lists, and result lists.

Security relies on default profiles that are also predefined. These profiles can be assigned to individual users and roles, addressing standard scenarios like read, edit, and administration access.

Additional customization options include creating new fields, establishing select lists for fields, and defining lists.

### Default Setting for the "File Cabinet" Functional Right
The configuration area requires users to possess the "Configure file cabinets" functional right, which administrators assign through DocuWare Configuration's User Management section.

A file cabinet represents a digital storage unit within a document management system where documents are organized and stored for long-term access.

Supported versions: DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Creating a New File Cabinet

### General
- **Name and description:** The file cabinet name displays in Web Client and DocuWare modules. Descriptions appear only on the Overview page.
- **Color:** The file cabinet symbol appears in the selected color in Web Client.
- **More options:** Database connections and storage locations are set up in DocuWare Administration.

### Database Fields
New file cabinets include 14 predefined fields by default:
Document Type, Company, Date, Contact, Customer ID, Email, Subject, Status, Pending Date, Document Number, Project, Amount, Tax number, IBAN

Field customization allows renaming, changing field types (Text, Numeric, Memo, Date, Keyword, Decimal, Date/Time), and adding new fields. Index tables require an existing file cabinet.

### Permissions
Four predefined permission profiles:

| Profile | Administrative | General | Field Rights | Overlay |
|---------|---|---|---|---|
| **Edit** | None | Store, Append, Edit index data, Edit documents, Checkout | Change, Allow new entries, Write | Add/Delete/Change annotations, Set stamps, Hide elements |
| **Read** | None | Search, Display documents, Export | Read, Search | None |
| **Delete** | None | Delete documents | None | None |
| **Owners** | Owners, Manage permissions, Operator, Manage dialogs | Store, Search, Display, Edit index data, Edit documents, Delete, Export, Append, Check out, View document history | Modify, Allow new entries, Write, Read, Search | Add/Delete/Change annotations, Set stamps, Hide elements |

**Administrative Permissions Impact:**
- Owners or Operator with Manage Dialogs/Permissions: All four sections visible
- Operator with Manage Dialogs only: General and Dialogs shown
- Operator with Manage Permissions only: General, Database Fields, Permissions shown
- Manage Permissions only: Permissions section only
- Manage Dialogs only: Dialogs section only

**Profile Allocation:**
- Document editing requires both Edit and Read profiles
- Document printing requires Read profile (includes Export rights)
- Non-creator administrators need Admin permission assignment
- Users need both dialog and permission assignments for document access

Supported versions: DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## File Cabinets - General Configuration

### Overview
Users can view created file cabinets and manage settings. The Operator right is required to edit settings.

**Important:** With DocuWare 7.13 and later, it is not possible anymore to delete a file cabinet that still contains documents.

### Full-Text Search
The full-text search finds entered terms in all index fields, in the document contents, in XML tags and—with DocuWare 7.12—annotations and stamps.

**Content Server:** Extracts text shots where all the document's index entries, words, and their position are noted. These transfer to the fulltext server.

**Fulltext Server Configuration:**
- Select data connection per file cabinet
- Multiple fulltext servers recommended for multiple cabinets
- Up to 100 pages indexed per file with Indexed pages per file (max.): 100
- Allow List / Blocking List for file types (cannot use both simultaneously)

**Reset Fulltext Options (DocuWare 7.10-7.12):**
1. Reindex Unprocessed Documents - checks for failed/unprocessed documents
2. Delete and Reindex Database Data - fastest option for wrong search results
3. Delete and Reindex All Data - required after configuration changes

### Version Management
Tracks document changes by saving multiple versions. The document being processed is locked; other users can view but not edit.

- Checkout function available in result list context menu
- Automatic version creation: documents auto-checkout on edit, auto-checkin on save
- Version history shows version numbers, status, storage date, comments, user
- Three statuses: Current, In progress, Out of date
- Version management can no longer be disabled once enabled
- Incompatible with unique field requirements and synchronization
- Document ID is identical for all document versions

### Security Options

**Document Encryption:** Documents stored encrypted; requires ENTERPRISE version. Administrators define symmetric key length. Documents stored before enabling cannot be encrypted retrospectively.

**Trusted Application User:** Users without DocuWare accounts can store documents (e.g., from MFP modules).

**Document Integrity Checksum:** Calculates checksum for all documents during storage. DocuWare 7.13 offers SHA-512 alongside SHA-256.

**High Security Level:** Requires enabling at organizational level and file cabinet owner must possess "High" security level. Once enabled, cannot be undone.

### Administrator Information
- GUID: automatically assigned identification number, cannot be changed
- Database Table Name: automatically assigned, cannot be modified
- Create File Cabinet Tables: allows setup of empty tables for recovery scenarios
- Index Data Backup: metadata saved fully in database as of DocuWare 7

Supported versions: DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## File Cabinets - Database Fields

### Overview
Database fields selected during file cabinet setup display properties including field type, length, document designation, and required field status. Fields can be added/removed, with changes automatically propagating to all dialogs.

### Field Types

- **Text**: Up to 2,000 alphanumeric characters
- **Memo**: At least 64 KB of storage capacity
- **Keyword**: Unlimited number of terms up to 255 characters each
- **Number and Decimal**: Up to 27 digits for decimal fields
- **Date**: Features a selector for default date fields
- **Date/Time**: Enables chronological sorting
- **Index Table**: Up to 50 columns and maximum 1,000 table rows (Text, Decimal, Date column types)
- **Satellite File Cabinet Fields**: Three automatic fields for document ID, modification time, synchronization status

### Database Field Properties
- **Name**: Maximum 50 characters
- **Required Field**: Must be filled in by the user
- **Predefined Entry**: Custom or dynamic (referencing user information)
- **Unique**: Entry may appear only once per file cabinet
- **Drop Leading Blanks/Zeros**: Removes fill-in characters during import

### Technical Notes
- MySQL limitation: maximum line of 65,535 characters
- Binary fields not processed by DocuWare
- Cloud users can prefix field names with "DW" for automatic database adjustment

Supported versions: DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## File Cabinets - Dialogs

The dialogs are composed of the available database fields. For a new file cabinet, DocuWare automatically creates dialogs for searching, storing, and displaying results.

Users can view all store dialogs they've created or been assigned. New dialogs can be created using a plus symbol. When copying a dialog, all settings are transferred except for the user rights.

**Important:** A new dialog must first be assigned to the users before they can use it.

Supported versions: DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Search Dialogs

Search dialogs enable users to enter filter terms for documents. They contain all custom database fields configured for a file cabinet. Fields can be hidden via an eye symbol without restricting access.

### System Fields Available
- Document identity
- Last modification on / Last modification by
- Saved on / Saved by
- File extension
- Document size
- Disk number

### Field Properties
- **Field name in dialog**: Customizable labels
- **Mandatory field**: Ensures important index information entry
- **Add wildcard to search**: Asterisk (*) displays index entries containing search terms
- **Predefined entry**: Auto-populated field values; dynamic entries reference logging fields
- **Read only**: Search executes with predetermined value only
- **Field mask**: Simplifies entry for formatted data
- **Select lists**: Organizational select lists can be enabled

### Select Lists Assignment
- **Internal**: System-generated with previously entered entries
- **Fixed**: Imported once and stored
- **External**: Retrieved dynamically with each field entry

Always select external select lists for date and number fields.

Supported versions: DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Store Dialogs

The store dialog appears in the Web Client when documents are filed. Users input index entries into dialog fields.

### Validation
Enable validation to ensure index entries are plausible or spelled correctly. Select a Web service based on REST.

### Intelligent Indexing Configuration
Enable "Use Intelligent Indexing to automatically fill Index Fields" in document tray configuration. The service automatically indexes documents.

### Field Properties

- **Field Name in Dialog**: Customizable labels
- **Mandatory Field**: Ensures important index information
- **Predefined Entry**: Custom, Dynamic (logging fields), or Automatic numbering
- **Read Only**: User cannot enter new index entry
- **Field Mask**: Simplifies formatted data entry
- **Select Lists**: Internal, Fixed, or External

**Select List Only**: Restricts field entries to select list values only.

### Filter Configuration
- Default select list: Enable fields for matching entries
- Multi-column select list: Set column and filtering conditions

Supported versions: DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Result Lists

A result list in the Web Client is set up like a table. One hit is shown per row. Users can reposition fields, hide fields, and modify sort order.

### Index Dialog
Opens when users select "Modify index entries" from context menu. "Edit" profile permission required.

### Field Properties
- Field name in dialog: Customizable labels
- Required: Mandatory fields for complete index information
- Field mask: Formatted entry assistance
- Select lists: Internal, Fixed, or External

For date and number fields, always select an external select list.

Supported versions: DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## File Cabinets - Lists

Lists function as result lists created through hidden searches without manual search dialog input. On-premises installations require the Task Manager License.

### Configuration Steps
1. Determine search criteria in the "Details" tab
2. Select a Result List for organizing results
3. Configure the Index Dialog for each document

### Rules Editor
- Select file cabinet fields and define rules
- Multiple rules with AND/OR logical operators
- System functions "User group" and "User role" for access restriction

### SQL Option
SQL enables complex filtering via WHERE clause. SQL join statements and substrings supported. Functional rights required for SQL command access.

**Forbidden SQL Commands:** ALTER, BEGIN, BACKUP, BULK, COMMIT, CREATE, DECLARE, DELETE, DENY, DROP, EXEC, EXECUTE, GRANT, GOTO, INSERT, KILL, MERGE, OPENDATASOURCE, OPENROWSET, PROC, PROCEDURE, RAISERROR, RECONFIGURE, RESTORE, RESTRICT, REVERT, REVOKE, ROLLBACK, SAVE, SHUTDOWN, SYSTEMUSER, TRAN, TRANSACTION, TRUNCATE, UPDATE, UNION, WAITFOR

Version 7.13+ includes syntax and validity checking for SQL commands.

Supported versions: DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## File Cabinets - Folder

Folder structures function like physical filing systems. Users select text fields and arrange them in a hierarchical structure.

- First field = top level
- Subsequent fields = lower levels
- Unlimited subfolders

### Folder Naming
Initial folder names derive from user-entered field data. Folder names can also be predefined using standardized retention schedules.

### Creating Empty Folder Structures
Click "[extended]" to establish empty folder structures. Select lists enable empty folders before document storage.

### Filter Setup
Filters limit the folder structure to documents matching specified rules.

Supported versions: DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## File Cabinets - Permissions

DocuWare provides four predefined permission profiles: Owners, Edit, Read, Delete. Custom profiles can be created.

### Permission Profiles

| Profile | Administrative | General | Field Rights | Overlay |
|---------|---|---|---|---|
| **Edit** | --- | Store, Append, Edit index data, Edit documents, Checkout | Change, Allow new entries, Write | Add/Delete/Change annotations, Set stamps, Hide elements |
| **Read** | --- | Search, Display documents, Export | Read, Search | --- |
| **Delete** | --- | Delete documents | --- | --- |
| **Owners** | Owners, Manage permissions, Operator, Manage dialogs | Store, Search, Display, Edit index, Edit docs, Delete, Export, Append, Check out, View history | Modify, Allow new entries, Write, Read, Search | All overlay rights |

### User-Defined Profiles
Administrators compile file cabinet and index field permissions for custom profiles.

### Index Value Profiles
Restrict access to specific documents based on defined criteria using graphical editor or SQL.

**Graphical Editor:** Select fields and define rules with AND/OR operators.

**SQL:** WHERE clauses for complex filters. Forbidden SQL commands apply (DocuWare 7.13+).

Supported versions: DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## File Cabinet Synchronization

Mirrors and synchronizes documents and index data between on-premises and Cloud systems. Only available for on-premises customers.

### Key Restrictions
- File cabinets with enabled version management cannot be synchronized
- All involved servers must use the same DocuWare version

### Use Cases
1. Weekly database comparisons between branch and central office
2. Backup transfers from on-premises to DocuWare Cloud

### Required Permissions
- Functional Right: "Configure file cabinet synchronization"
- File Cabinet Rights: Display, Store, Search, Delete
- Field Rights: Write, Allow new entries

### Deleted Document Synchronization

| Source Condition | Target Outcome |
|---|---|
| Document in trash bin | Document moved to trash bin |
| Deleted document restored, still in source trash | Document restored with source data |
| Deleted document restored, permanently deleted in target | New document created |
| Document permanently deleted in source | Document remains in trash bin |

### Scheduling
- Manual: "No repeat" setting with "Start once"
- Automatic: minimum ten-minute interval recommended
- Jobs must be enabled to execute

Supported versions: DocuWare on-premises 7.10, 7.11, 7.12, 7.13

---

## Document Relations

Documents are frequently interconnected (delivery notes with invoices, emails with project plans). Document relations enable quick access to associated information.

### Linkage Rules
- **Index/System Field**: Select field from target file cabinet
- **Operator**: Varies by field type (text, date, numerical)
- **Entry Types**: User-specific, Predefined (dynamic), or Field of source file cabinet
- **Multi-Rule Combinations**: AND or OR operators

Supported versions: DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Autoindex

Autoindex enables automatic indexing by transferring metadata from external systems into the file cabinet. Uses a "match code" to align records.

### Capabilities
- Extract field contents from external records as index entries
- Assign fixed or dynamic entries to documents
- Copy index entries to external data records
- Write fixed or dynamic entries back to external sources

### Limitation
Does not process binary database fields. Memo fields hidden from interface.

### Configuration

- **Trigger**: Scheduling intervals minimum 60 minutes; immediate processing via file cabinet event trigger
- **Data Source**: File cabinet database, text file (read/write, read-only, copy modes), filter capabilities
- **Matchcode**: At least one matching field; excludes fulltext, keyword, memo fields
- **Processing List Direction**: Iterate through file cabinet or external data source first

### Assignment & Writeback
- **Assign Data**: Field contents, fixed entries, or system entries with overwrite options
- **Write Back**: Add/modify external data source entries

### Matching Scenarios
- **Multiple Matches**: Keyword fields or last-record selection
- **No Matches**: Flag unmatched records or create new entries

Requires purchased Autoindex license.

Supported versions: DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Field Masks

Field masks restrict user input for text and keyword fields to defined formats. DocuWare provides predefined masks and allows custom definitions.

### Mask Definition (Regular Expressions)
- `[A-Za-z0-9]`: Latin characters or numbers
- `[0-9]`: digits 0-9
- `[A-Z]`: uppercase letters
- `\d`: numbers
- `?`: preceding expression optional
- `{n}`: exactly n occurrences
- `{n,n}`: n to x occurrences

### Common Patterns
- **IBAN**: `[A-Z]{2}[0-9]{2}[A-Za-z0-9\s]{11,30}`
- **BIC/SWIFT**: `[A-Z]{6}[A-Z0-9]{2,5}`
- **ISBN**: `(\d{3}-\d{1,5}-\d{1,7}-\d{1,7}-\d)`
- **VAT (Germany)**: `\d{9}` (preceded by "DE")
- **VAT (EU)**: `[A-Z]{2}[A-Z0-9][A-Z0-9]\d{5}[A-Z0-9]{0,5}`
- **International Telephone**: `\+\d{2}\d?-\d{2}\d{0,2}?-\d{3}\d{0,7}`
- **German Postal Code**: `[A-Z][A-Z]?-\d{4}\d?`
- **Time**: `(0?\d|1\d|2[0-3])\:[0-5]\d\:[0-5]\d`

### Important Notes
1. Field masks don't apply to automatic storage events
2. Users can bypass masks in index dialogs unless masks are defined there
3. Avoid leading/trailing spaces in mask definitions
4. List longer patterns first when alternatives exist

Supported versions: DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Select Lists - Indexing Assistance

Select lists help users enter data into index fields by displaying predefined entries. They prevent typing errors and maintain data consistency.

### Access Requirements
- "Configure select lists" functional right needed
- "Edit Fixed Select Lists" right for direct editing from store dialogs

### Three Select List Modes
- **Internal**: Based on previous field entries or internal databases
- **Fixed**: Imported once, stored for quick access
- **External**: Retrieved dynamically, real-time synchronization

### Table Types
- Single-column: cannot be filtered
- Multi-column: support filtering based on other dialog fields

### Creating Select Lists
1. Define Mode (Fixed or External)
2. Select Data Source (file connections, database, file cabinets, local file uploads)

**File Import:** Single-column = TXT format; Multi-column = UTF8-coded CSV with semicolon separator.

### Multi-Column Select Lists and Dependent Filtering
Selecting a value in one field automatically filters options in related fields.

### Implementation
- **Web Forms**: Configure in Forms Designer; "Autofill Single Value" auto-populates linked fields
- **Store Dialogs**: Enable in field properties, specify table column, configure filter conditions

### Cloud vs On-Premises
Cloud users cannot access database connections for security; use file connections instead. File cabinets work as select list sources for both.

Supported versions: DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## DocuWare Validation

Validation ensures documents are stored with accurate data by checking entries against server-side rules. Documents failing criteria are not stored.

### Examples
- Validate dates against system date
- Prevent values exceeding limits
- Check customer numbers against CRM systems

### Technical Implementation
Index data validation operates through a REST-API web service. Users choose their programming language. Applied in DocuWare Configuration > File Cabinets > Store Dialogs.

Previous validation forms remain supported in v6.12. Future versions plan to support only web service-based validation.

Supported versions: DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Setting Up Intelligent Indexing

Intelligent Indexing automatically categorizes documents and identifies relevant index words. Users confirm or refine suggestions, enabling self-learning.

### How It Works
1. Scan documents into enabled document trays
2. Green-marked documents store automatically (reliable indexing)
3. Other documents require verification
4. User corrections train the system

### Implementation Types
- **Web-Based Service (DocuWare Cloud)**: Configure store dialog, assign to document tray
- **On-Premises Web Service**: Activate, configure store dialog, assign to document tray
- **On-Premises Add-On Module**: Install, configure store dialog, assign to document tray

### Configuration
Access via DocuWare Configuration > Indexing > Intelligent Indexing

**Enable**: Activates service (required for on-premises only)

**Configure - Store Dialog:**
- Required for each file cabinet using Intelligent Indexing
- One store dialog per cabinet recommended
- Enable "Use Intelligent Indexing to automatically fill Index Fields"
- Link fields and specify language

**Configure - Document Tray:**
- Assign configured store dialog to tray
- Only ONE store dialog per tray
- Multiple trays needed for multiple dialogs

**Customize**: Modify index terms for automated processes

Supported versions: DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Use Intelligent Indexing

### Color-Coded Reliability
- **Green**: All fields reliable; auto-store possible
- **Yellow**: Less certain suggestions
- **Red**: Unreliable or no suggestions

### Storing Documents
Fields are color-coded in store dialog. Users can correct entries or use "Point and Shoot" to transfer terms from the Viewer. Index Card View shows dynamically displayed, color-coded suggestions.

### Tips for Best Results

1. **One-Click Indexing Over Keyboard**: Select text from documents to teach word positioning
2. **Index Uniformly**: Consistent terminology; multiple incorrect entries need multiple corrections
3. **Link Default Fields Correctly**: 42 total fields (11 default, 31 custom); default fields have background rules improving hit rates
4. **Match Field Types**: Date info → date fields; numeric → numeric fields
5. **Ensure OCR Quality**: Min 300 dpi (B&W) or 200 dpi (color)

Supported versions: DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Customize Intelligent Indexing

### Example 1: Adapt Document Type Names
Different workflows may require distinct terminology. Navigate to DocuWare Configuration > Intelligent Indexing > Area 3 Customize > Change Name of Document Types.

### Example 2: Compare with External Data Sources
Cross-reference results against data from other business systems. Extract company name lists from ERP systems and integrate via field filters. Access DocuWare Configuration > Intelligent Indexing > Area 3 Customize > Change Field Filter.

Supported versions: DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Technical Insights: Intelligent Indexing

### Architecture
Self-learning algorithms recognize common document types and suggest relevant index words.

**Data Centers:**
- Amsterdam (Netherlands) - EMEA region
- Virginia (USA) - North and South America
- Tokyo (Japan) - Japanese customers
- New South Wales (Australia) - Asia-Pacific

Infrastructure runs on Windows Azure with Intelligent Indexing Service computers and SQL Azure database.

### System Integration
On-premises customers register separately and receive XML configuration. Cloud customers have pre-configured access.

### Workflow
1. Document enters configured document tray
2. Full-text extractions generated and transferred
3. Service analyzes and searches for similar known documents
4. Suggested index words offered with confidence indicators (traffic light system)

### Index Recognition
- Multiple methods with patents in Germany and USA
- High performance across numerous algorithms per document
- Flexible multi-language and cultural processing
- Handles skewed scans
- Analyzes document elements regardless of page location

**Learning:** The more reference documents read, the higher the accuracy and reliability.

### Model Space
Organization-specific storage for learned information. Full-text excerpts strictly separated from other organizations' data.

### Security
- HTTPS encryption for all communications
- Microsoft Azure database stores extractions, index data, feedback, metadata
- Access controls with user/roles structure
- Data deletion available upon request
- Complete data removal when discontinuing service

Supported versions: DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Document Tool (On-Premises)

Command-line utility for managing documents with three primary operations.

### Index Restore
Restores backup index data (index entries, annotations, stamps) to the database. Avoid using for synchronized file cabinets (risk of duplicates).

### Migration
Moves documents within file cabinets between disks. Used to reduce disk sizes, combine disks, or relocate documents.

### Encryption
Encrypts existing documents retroactively.

### File Locations
- v7.10 and earlier: `…\DocuWare\Background Process Service\`
- v7.11 and later: `…\DocuWare\PowerTools\DocumentTool`

### Command Line Parameters
| Parameter | Description | Status |
|-----------|-------------|--------|
| filename | XML settings file | Required |
| jobtype | 0=Index Restore, 1=Migration, 2=Encrypt | Required |
| username | DocuWare username (must be file cabinet owner) | Required |
| password | User password | Required |
| orgaguid | Organization GUID (multi-org systems only) | Optional |

### Settings File Parameters
| Parameter | Description |
|-----------|-------------|
| fileCabinetGuid | Target file cabinet GUID (required) |
| destinationDiskNumber | Target disk (migration only) |
| DocumentsFilter | Optional document filtering |

### Filter Criteria
- Storage date range
- Modification date range
- Document ID range
- Disk numbers

Recommendation: Add as scheduled task in Windows Task Scheduler.

Supported versions: DocuWare on-premises 7.10, 7.11, 7.12, 7.13

---

## System Administration (On-Premises)

DocuWare Administration covers primarily the administration and maintenance of the DocuWare Server required for on-premises systems.

Version-specific documentation:
- DocuWare Administration 7.9
- DocuWare Administration 7.8
- DocuWare Administration 7.7

---

## Backup (On-Premises)

It is essential to guarantee business continuity by maintaining operational status for the DocuWare system at all times.

### Availability
Scalability enables redundancy through multiple server installations. Geographically distributed systems are complex and recommended only with DocuWare Professional Services input.

### Data Backup
There is no DocuWare mechanism that automatically backs up data. IT department bears responsibility.

**Databases to Back Up:**
- DWSYSTEM: system and organizational data
- DWDATA: internal search and document discovery
- DWNOTIFICATION: email notifications (optional)
- DWWORKFLOWENGINE: process automation data

**Storage Location Contents:** File directories in network locations storing documents, archives, mailbox files.

**System Storage:** Directory containing DocuWare Forms data.

**Full Text Files:** Full-text server catalog files. Emergency restoration possible from database if backup unavailable.

**Configuration Files:**
1. Server Settings: %ProgramData%\DocuWare
2. DocuWare Desktop Settings: %ProgramData%\DocuWare\Desktop (or %LocalAppData%\DocuWare\Desktop)
3. COLD Configurations (DocuWare 5.x): Legacy configurations

Supported versions: DocuWare on-premises 7.13, 7.12, 7.11, 7.10
