# DocuWare Knowledge Center - Basics

---

## Login and Authentication

DocuWare implements OAuth2 authentication across all internal services and user-accessible components including Desktop Apps (DocuWare Printer, Import, Scanner, SmartConnect, Edit&Send, Connect to Outlook, Windows Explorer Client, Workflow Designer), Export, User synchronization, Local Data Connector, Make Connector, Power Automate Connector, and Mobile Applications.

### Initial Login and Credential Requirements

Upon first launch of these applications, users must enter credentials. For security reasons, the credentials must be entered again if the application is not used for 31 days.

Additionally, Connect to Outlook, Windows Explorer Client, and Workflow Designer require credential re-entry after 90 days.

### Access Management

Users can review active application sessions through the Web Client main menu under Profiles and Settings > Security. This section provides visibility into all logged-in applications.

Access revocation is available here, though applications may remain active for approximately one hour post-revocation. Following this period, a login screen appears requiring fresh credentials.

**Supported versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10
**Tags:** Security

---

## Get Started (Help for Web Client)

This is the entry point for the DocuWare Web Client help documentation.

---

## Web Client Overview

The DocuWare Client is the central platform for your business documents. Depending on whether you work with the trial version of DocuWare or with an existing system, some settings in DocuWare Client differ, but the functions are the same.

### Overview of the DocuWare Client Areas

1. **Your Inbox** - Capture documents, prepare them in your individual document tray for archiving and store them to the file cabinet.

2. **Access the file cabinet** - Find your archived documents quickly, collaborate and list your daily tasks.

3. **Work area** - The work area offers different functions depending on whether you have selected a document tray or another element. Users can open multiple work areas simultaneously.

4. **View documents** - If you double-click on a document in the document tray, it will be opened here in the viewer. Users can annotate documents in the viewer.

5. **Main menu** - Accessible by clicking the username, containing:
   - Profile and settings
   - Configurations
   - Touch Mode
   - Desktop Apps
   - Mobile Apps
   - Help & Info

**Supported versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10
**Tags:** Getting started, Out of office

---

## The Document Tray

A temporary storage area in DocuWare where documents can be viewed and processed before being stored in a file cabinet.

A document tray in DocuWare is primarily used to process documents before they are stored.

### How Documents Enter Trays

1. **Drag and drop** from desktop or file explorer
2. **Import button** in toolbar to open file selection window
3. **Scan button** in toolbar for locally connected scanners (requires Desktop Apps installation)
4. **Network scanner** import through administrator-configured settings

### Available Functions

1. **Display** - Double-click documents; use "Open in new viewer window" or [Ctrl]+[Alt]+[Enter] for comparisons
2. **Merge documents** via stapling (PDF creation) or clipping (preserves formats)
3. **Edit** using default programs for file types
4. **Rename** documents via [F2]
5. **Print** individually or in bulk with annotation options
6. **Download or email** with format conversion options
7. **Delete** to recycle bin (permanent deletion after 30 days)

**Supported versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10
**Tags:** Getting started, Import

---

## Store Documents

Double-click a document from the tray, then click Store. When multiple store dialogs exist, select the one matching your target file cabinet (formatted as "<file cabinet name> - <Dialog name>").

### Index Assignment

Now is the latest point at which you can assign index entries or, in other words, classification criteria to the document. Index data enables document discovery, folder structuring, and workflow management.

### Pre-filled Fields

Index fields may already contain data from scan/import configurations or enabled Intelligent Indexing. Colored indicators reflect reliability: green (highly reliable), yellow (less reliable), red (unreliable/no suggestion).

### Manual Entry Options

1. **Select List Method:** Click field arrows to choose suitable terms
2. **One Click Indexing:** Click document content to populate active fields without typing, reducing errors and moving focus automatically to next fields
3. **Multi-selection:** Hold [Ctrl] while clicking multiple words for single fields

### Date Field Tips

Press [x] for current date entry; use [+] and [-] to adjust by single days.

Click Store when all mandatory fields are completed.

**Supported versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10
**Tags:** Getting started, How-to, Import, Indexing

---

## Retrieving Documents

DocuWare enables rapid retrieval of documents from thousands stored in the system through multiple search approaches tailored to different working styles.

### Four Search Method Categories

1. **Selection from Existing Lists** - Users access index field select lists by clicking arrows next to search fields to choose predefined terms.

2. **Full-Text Search** - This method searches document content using terms without requiring specific field placement. You enter a term in the search field and all documents containing this term will be displayed. Hits display with color coding — first match in red, subsequent matches in yellow.

3. **Keyword Search with Asterisk Capability** - Keywords represent classification criteria (index entries). Users must enter terms in appropriate fields. The asterisk wildcard enables partial matching, such as "Peters*" finding variations like "Peters Engineering" or "Peters & Partner."

4. **General Rules for All Methods**
   - Access search dialogs via the top-left tab section
   - Multiple dialogs typically exist (shown as <file cabinet name> - <dialog name>)
   - Documents must be stored in file cabinets, not document trays
   - Double-click results to open; right-click displays context menus
   - Combine methods to refine results

### Glossary Terms

- **Index Field:** A predefined DocuWare categorization tool
- **Select List:** Predefined list of terms
- **Result List:** A tabular display of documents matching search criteria
- **File Cabinet:** A digital storage unit for long-term document access
- **Document Tray:** A temporary storage area before filing

**Supported versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Displaying Documents

Double-click documents to open them in the viewer from document trays or result lists. The viewer offers extensive functionality beyond basic viewing and page scrolling.

### Title Bar
Contains viewer functions including navigation elements, stamps, and zoom tools. All elements also appear in the comprehensive toolbar.

### Toolbar Organization
Click the small downward arrow in the upper left corner if the toolbar isn't visible. Hovering over icons displays function descriptions. Functions are divided into seven areas.

### Seven Toolbar Areas

**1. Navigation:** All functions for scrolling through the pages of a document and for switching from one document to the next.
- Navigate through documents (switch between documents)
- Navigate through pages (scroll within current document)
- Navigate through document files (when documents contain multiple files)

**2. Tools:** Document functions including edit, print, send, and index entry display.
- **One Click Indexing:** Words, dates, or even numbers are marked as an area as soon as you move the cursor over the document.
- **Full-text search:** Search and highlight specific terms with navigation capabilities
- **Copy text to clipboard:** Extract text from scanned or digital documents
- **Retrieve link to document:** Generate shareable links for internal document references
- **Send inquiry:** Request colleague approval with workflow control and decision tracing via stamps
- **Zoom into selected zone:** Enlarge specific document sections without zooming the entire document

**3. Display:** Zoom, rotation, display improvement, and annotation layer visibility options.

**4. Stamps:** Available stamps vary by file cabinet storage location.

**5. Annotations:** Text, highlighting, and redaction tools for the annotation level.

### Annotation Layers

Picture annotation layers like sheets of clear plastic film that can either lay on top of a document or removed as needed.

Purpose: Preserve archived documents (invoices, tax documents) while allowing notations.

**Features:**
- Five separate, independently controllable layers (numbered 1-5)
- Visual indicator (pen icon) shows currently active layer
- Click numbers to show/hide layers

**Annotation Types:** Stamps, text, markers, freehand lines, straight lines, arrows, rectangles, and ellipses (opaque or transparent options).

**Editing Annotations:** Select the thick arrow tool, click the annotation to edit, then move or delete using the Delete key or Delete object tool (thick X).

**Merge Annotations:** You should keep in mind that this step cannot be undone and the document is no longer stored as the original. Exception: Automatic versioning creates new documents while preserving originals.

**6. Overview:** Thumbnail display of all document pages.

**7. Linked:** Access predefined related documents via links.

**Supported versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10
**Tags:** Getting started, How-to

---

## Trash Bin: Restoring Documents

The DocuWare trash bin allows users to recover accidentally deleted documents. Documents deleted from result lists, task lists, automation jobs, the Platform Service, file cabinet synchronization, and document transfers are moved to this virtual trash bin.

### Key Features
- Documents in the trash bin can be restored to original locations or permanently deleted
- Automatic removal occurs after a fixed 30-day retention period
- Restore operations return the document to its original storage location without triggering workflows or notifications
- All trash bin operations are logged in document history

### Requirements
No separate permissions or licenses are needed. All users have access to the trash bin function in both DocuWare Cloud and on-premises versions.

### Web Client Usage
Each user has a personal trash bin accessed via "Recently deleted." The interface allows:
- Viewing system data (document name, deleting user)
- Sorting and filtering columns
- Batch operations on single, multiple, or all documents
- Display of remaining days before 30-day deletion
- Immediate functionality without additional configuration

**Important:** Keep the Recently deleted window open during deletions; closing it cancels the process.

### Permissions Structure
- File cabinet owners see all deleted documents
- File cabinet users see only their own deletions
- Document tray users see documents deleted from their trays
- Users without permissions see nothing

### Storage Considerations
Deleted documents count against storage quotas for 30 days. Quota is released only after final deletion.

### Legacy Document Limitations
- No change in the Changed by / Changed on fields when deleting and restoring
- Viewer highlighting is lost during restoration

---

## Profile & Personal Settings

Manage your DocuWare account: update profile details, adjust settings, and enhance security with two-step verification in the Web Client.

The Profile & Settings section functions as each user's personal control center where users modify account details, interface preferences, and security options. Changes take effect immediately across the Web Client.

### Profile Tab
- **Personal data:** Users can edit name, email, or salutation.
- **Out of office:** Set yourself as out of office, so that your workflow tasks will be forwarded to another user.

### General Tab
- **Region:** Users may switch the DocuWare interface language, with Help links for English, German, French, Spanish, and Japanese opening in the browser's language rather than the DocuWare interface language.

### Security Tab

#### Password Management
You will need your old DocuWare password to create a new one.

#### Two-Step Verification
Two-step verification requires two independent identity proofs:
1. Username and password entry
2. Time-based one-time password from an authenticator app

Benefits: DocuWare allows access only after both factors are confirmed, minimizing the chance of unauthorized logins even if a password is compromised.

#### Activation Steps
1. Download authenticator app compatible with TOTP (time-based one-time password)
2. Navigate to DocuWare Client > Profile & Settings > Security
3. Click Activate to display QR code
4. Open authenticator app on mobile phone
5. Scan the QR code
6. Enter the first six-digit password and click Verify
7. System displays success message and automatically logs user off
8. Next login prompts for credentials and one-time code

#### Lost Device Protocol
If the mobile phone of a DocuWare user is lost, it is not possible to login into DocuWare. The DocuWare administrator can deactivate two-step verification through DocuWare Configurations > User management.

#### Configurations Using Your Account
Automated jobs — such as workflows and notifications — are executed with a specific DocuWare user account and inherit that user's permissions. Revoking credentials stops jobs immediately; restart requires DocuWare Configurations access.

### Document Trays Tab
- Users can hide trays using the eye icon, sort them, and change the default tray.
- All store dialogs assigned to you are listed here.

### Searches Tab
- **Search Dialogs:** Users can hide and sort assigned search dialogs.
- **Result Lists:** Each result list is used by a search dialog above. Users can hide fields and sort.
- **Multiple File Cabinet Search:** All searches across multiple file cabinets are stored here. These steps will allow you to store the combination of file cabinets and search dialog used, but not the actual search term.

### Forms Tab
All DocuWare forms assigned to you are listed here.

### Viewer Tab
Users can select three viewing options:
- Show DocuWare Viewer in the same window
- Open DocuWare Viewer in a new window
- Open DocuWare Viewer with index dialog in a new window

**Viewer Toolbars:** Click the eye icon to hide tools you do not need.

**Supported versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Searching with Operators

When searching in DocuWare, certain words and characters function as logical operators rather than search terms. Special handling is required when the index term contains elements like AND, OR, quotation marks ("), question marks (?), or backslashes (\).

### Escaping Special Characters

| Search Term | How to Enter |
|---|---|
| MILLER AND SON | "MILLER AND SON" |
| NOW OR NEVER | "NOW OR NEVER" |
| Program "Othello" | Program \\"Othello\\" |
| Clever?123 | Clever\\?123 |
| C:\Documents | C:\\\\Documents |
| Price List (UK) | Price List \\(UK\\) |

### Search Operators (Text/Content Fields Only)

- **AND**: `*Miller* AND *Son*` locates documents containing both terms
- **OR**: `*Miller* OR *Son*` finds documents with either term
- **NOT**: `NOT *Miller*` returns documents without the specified term
- **EMPTY()**: identifies documents where the index field contains no data
- **NOTEMPTY()**: identifies documents where the index field contains data
- **CURRENTUSERSHORTNAME()**, **CURRENTUSERLONGNAME()**, **CURRENTUSEREMAIL()**: user-specific search functions

### Additional Guidelines
- Placeholder searches with asterisks (*) exclude external select list proposals
- OR searches in keyword fields require direct execution without clicking the Plus icon
- Fulltext searches should avoid periods, which function as word separators

**Supported versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10
**Tags:** How-to, Search

---

## Save Frequent Searches as List

Access documents that you need frequently — without having to enter search terms. You simply save a search in the DocuWare Client and retrieve all incoming invoices, for example.

### Steps

1. Search for your documents as usual.
2. When the results are displayed, click on the options in the top right-hand corner of the result list and select Save this search as a list.
3. Give the search a name. Afterwards the search is displayed in the Lists area and is available as a result list at the click of a button.

The result list is updated automatically when a new document is stored that matches the search.

**Supported versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10
**Tags:** Getting started, How-to, Search

---

## One Click Indexing

One Click Indexing is a tool found in DocuWare's Viewer — a great way to quickly assign index terms when filing.

### How It Works
The tool activates when a document is open in the Viewer and ready for storage. When moving the cursor over a document, words, dates or even numbers are immediately highlighted in color as a range. Clicking transfers content to the active store dialog field, with the cursor automatically advancing to the next Index Field.

This eliminates tiresome typing as well as potential typos and transposed numbers and prevents workflow delays caused by manual entry errors like missing invoice digits, misspelled vendor names, or transposed IBAN numbers.

### Five Tips for One Click Indexing

1. **Activation:** Enable via the Tools section of the DocuWare Viewer toolbar; customize the toolbar if the icon is missing.
2. **Multiple Terms:** Hold [Ctrl] to select several words simultaneously for transfer to a single field (example: first and last names).
3. **File Properties:** Transfer clickable file properties from the Viewer footer (file name, type, and date).
4. **Extended Use:** Functional in index dialogs and workflow tasks for archived documents.
5. **Intelligent Indexing:** Compatible with Intelligent Indexing systems, improving their accuracy.

**Supported versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10
**Tags:** Getting started, How-to, Indexing

---

## Customizing the Viewer Toolbar

(Content not available — page rendered dynamically)

---

## File Formats Supported by the Viewer

The DocuWare Viewer (Version 7.6+) supports an extensive range of file formats for document display in the Web Client.

### Document Formats
PDF (pure XFA PDFs; excluding portfolio PDFs) and numerous raster image formats including JPEG, TIFF, PNG, GIF, BMP, and HEIC variants.

### Office & Productivity
- **Microsoft Office:** Word documents (DOC, DOCX, RTF, and template variants), Excel spreadsheets (XLS, XLSX, XLSB, and related formats), PowerPoint presentations (PPT, PPTX, PPS, and associated types), and Outlook email files (MSG, PST, OST, OFT).
- **OpenOffice:** ODT, OTT, ODS, and ODP files.

### Specialized Formats
- **AutoCAD:** Drawings from Versions R2.5/2.6, R9, R10, R12, R13, R14, R2000/2002, R2004/2005/2006 through 2017 releases
- **Email:** EML, EMLX, MBOX
- **Web:** HTML, MHTML
- **Text:** TXT, CSV, TSV
- **Archive:** ZIP, RAR, 7Z, and others

**Supported versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Displaying XML Invoices

The DocuWare Viewer handles electronic invoices in XML format by rendering them in a readable format resembling PDF invoices. This functionality relies on style sheets published by national standard authorities and organizations, which undergo regular updates.

**Important:** Changes in the new version of a style sheet can also affect the display of XML invoices in DocuWare. This means that annotations or stamps may be found in different positions than in an earlier style sheet version.

### Style Sheets
DocuWare utilizes a style sheet for the EN 16931 European format, issued by German Koordinierungsstelle für IT-Standards (KoSIT). Since only KoSIT published this style sheet for the European standard, XML invoices display exclusively with German labels.

**Supported versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10
**Tags:** Import

---

## Folder

The hierarchical folder view in the Web Client is convenient both for storing documents, as well as for the search of already stored documents. The folders will be set up within the file cabinet administration.

**Related Resources:**
1. Project Folders — A Simple Way to Store Documents
2. Searching for Documents in Folders with DocuWare

**Supported versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Keyboard Usage

For convenient working, you can use the following keyboard shortcuts in DocuWare:

### General Navigation
- Menu navigation uses arrow keys (up/down)
- Escape closes menus and submenus

### Main Navigation Shortcuts
- Document trays: Ctrl + Shift + 1
- Searches: Ctrl + Shift + 2
- Lists: Ctrl + Shift + 3
- Tasks: Ctrl + Shift + 4
- Second workspace variants: Ctrl + Shift + 5-8

### Document Tray Operations
- Movement: Arrow keys
- Open document: Enter, Ctrl+Alt+Enter
- Edit: Ctrl+Alt+Space
- Delete: Del
- Rename: F2
- Clip: Ctrl+Alt+C
- Staple: Ctrl+Alt+T
- Send/Download: Ctrl+Alt+S / Ctrl+Alt+D
- Print: Ctrl+Alt+P
- Check-in: Ctrl+Alt+V
- Index: Ctrl+Alt+X
- Context menu: f

### Search Dialog
- Search: Enter
- Reset: Ctrl+Alt+R
- List navigation: Arrow keys
- Date shortcuts: + / - / X

### Store Dialog
- Autofill indexing: Ctrl+Alt+J
- Smart Index: Ctrl+Alt+K

### Result/Task Lists
- Navigation, opening, editing, deletion, clipping, sending, and history viewing shortcuts

### Viewer
- Page navigation: Arrow keys
- Split view: Ctrl+Alt+Comma
- Zoom: + / -
- Layer toggling: Ctrl+Alt+F8 through F12
- Drawing tools: 1-0 keys

**Supported versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Filtering Documents Based on Index Criteria

(Content not available — page rendered dynamically)

---

## Stamps

Stamps speed up and simplify document processing. In DocuWare Viewer, they are set to an open document.

Two primary functions:
1. **Additional document information** - As with an analog stamp, you apply graphic or text elements to a document.
2. **Modifying index entries** - With the appropriate configuration, a stamp can change the entries in the database fields.

### Application Example
Invoice processing workflow demonstrating status change from "New" to "Approved" triggering document forwarding to finance.

### Default Settings
Every DocuWare user can create stamps for themselves. Users with Configure stamp functional rights can create stamps for others. Only accessible file cabinets display in configuration.

### Text Stamp
Can contain user names, dates, or user input fields for information like cost center entries.

### Bitmap Stamp
PNG, JPG, and GIF are supported as formats for the image element. The maximum image size is 850 x 600 pixels.

### File Cabinet Selection
Stamps can be assigned to specific cabinets or used across all cabinets.

### Indexing Options
Database fields can be selected for modification when stamp is applied. Setting: Stamp will not be set if the stamp data does not match any of the fields.

### Behavior Settings

**Save Options:**
- Immediately (default)
- If the document is saved

**Document Behavior:**
- Document remains open
- Open next document automatically
- Close document

**Additional:** Stamp remains active and can be used several times in a row

### Signature Feature
Enable this option to use the stamp as a simple signature.

Restricted actions after signature stamp placement:
- Editing page content
- Adding non-signature stamps
- Placing annotations
- Merging annotations
- Applying automatic image enhancement

Index value modifications remain permitted.

### Password-Protected Stamp
Users must enter DocuWare password. If the company uses single sign-on, the DocuWare password may be unknown to the user.

### Permissions
Direct user assignment or profile-based assignment available. Password protection option mentioned.

**Supported versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Supported Languages

DocuWare offers support across 24 languages with varying availability across different components.

### Language Support

- **DocuWare Client and Configuration:** All 24 languages supported
- **Desktop Apps:** All 24 languages supported
- **DocuWare Mobile:** 20 languages (excludes Arabic, Croatian)
- **DocuWare Administration:** Limited to 6 languages: German, English, Spanish, French, Italian, Japanese, and Chinese Traditional

DocuWare Administration is only used for a few settings in locally installed DocuWare systems and is therefore only available in the main languages.

### Language Selection

- **DocuWare Client and Configuration:** Set via DocuWare Main Menu > Profile & Settings > General
- **Desktop Apps and Administration:** Use client computer's regional settings
- **DocuWare Mobile:** Adapts to device's native language preferences

**Supported versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Find Help for Your DocuWare Version

You are in the DocuWare Knowledge Center. Find information about DocuWare and how to use it:

1. **Help for DocuWare Cloud and DocuWare on-premises version 7.13 - 7.10** — Each article shows the version to which it applies. Version-specific differences are highlighted accordingly.

2. **Help for DocuWare Preconfigured Solutions**

3. **News and Release Notes (What's new) for DocuWare version 7.13 - 7.10** — Switch to the category News.

### Important Notice
Availability of DocuWare Help: The availability for the help of a DocuWare on-premises version ends with the official support period for that version. This means that DocuWare help is currently available for on-premises versions 7.8 to 7.13.

### Previous Versions
- **Version 7.9:** Help available at previous Knowledge Center. Help for version 7.9 will be offline with the end of DocuWare support for version 7.9 on 31. October 2026.
- **Version 7.8:** Help available at previous Knowledge Center. Help for version 7.8 will be offline with the end of DocuWare support for version 7.8 on 31. May 2026.

---

## DocuWare Desktop Apps

The DocuWare Desktop Apps allow users to perform various functions including scanning documents to trays, sending documents from trays or file cabinets, and editing documents in native applications within DocuWare.

### Available Desktop Apps

1. **Connect to Outlook** - Store email in DocuWare via Outlook menu
2. **Edit & Send** - Edit or send documents directly from DocuWare
3. **Import** - Automatically import documents from monitored folders
4. **Printer** - Print and store documents from any application as PDF
5. **Scan** - Scan documents into trays or file cabinets
6. **Export** - Export index data for third-party application transfer
7. **Smart Connect** - Display matching DocuWare documents from other applications
8. **Windows Explorer Client** - Integrate DocuWare into Windows File Explorer

### Administrative Apps
The Workflow Designer is initially the only relevant tool for creating workflows or editing pre-configured workflows.

### Installation Process
- Access main menu (user name) and select Desktop Apps > Install Desktop Apps
- Wait for setup download and run by double-clicking
- Select needed applications
- Follow setup instructions
- Link apps via Desktop Apps > Link Desktop Apps in Web Client menu

**Supported versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10
**Tags:** Getting started

---

## Expertise for Everyday Work

(Category landing page — content rendered dynamically)

---

## Processing Documents

### Indexing

**Index fields:** Text extracted from documents can be refined using an Edit function. As of DocuWare 7.7, dynamic entries can also be edited.

**Text field capabilities:**
- **Define text:** Specify text subareas for indexing by determining whether to use text after, before, or between specific strings; specify exact positions; define field delimiters; select specific entries; choose lines from multi-line barcodes
- **Correct text:** Replace individual characters to fix readout errors (e.g., "1" misread as "I")
- **Replace text:** Replace all read-out text of an area with other text, with option to create replacement lists

**Additional options:** Date fields support format specification; numeric fields support format specification based on regional settings.

### Identify

DocuWare can automatically select correct configurations based on document type during scanning, importing, or printing. This requires enabling "Select configuration automatically" under Source settings. When using DocuWare Printer, configurations can be identified from source applications like MS Word if a sample document was printed with the appropriate metadata.

### Splitting

Documents can be split using three criteria:
- **Fixed page numbers** — e.g., two-page form letters split after specified page count
- **Text criteria** — e.g., invoices split before terms and conditions using text criteria like "Total"
- **Barcode changes** — e.g., batch scanned documents with individual barcodes split upon barcode value changes

Sample documents are required for text-criteria splitting.

### Letterhead

Letterheads or logos can be added to first pages only or all pages. The letterhead is automatically positioned left-aligned at the top. For documents with picture or color backgrounds, enable "Letterhead always in foreground" to prevent coverage. This feature combined with Electronic Signature creates PDFs instead of PDF/A files.

**Limitation:** XML documents and PDFs that contain an XML as attachment do not support Letterhead as a function.

**Supported versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10
**Tags:** Indexing
