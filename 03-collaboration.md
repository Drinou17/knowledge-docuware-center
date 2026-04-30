# DocuWare Knowledge Center - Collaboration

---

## Forms

DocuWare Forms enables creation of web-based forms without coding. The platform supports text fields, check boxes, drop-downs, calendar inputs, file uploads, and more for data capture.

Each web form includes configuration settings for fields, indexing, storage location, and access rights. Users access forms via links and submit them as PDFs to file cabinets with a single click. Submitted forms are stored automatically and are immediately available to all authorized DocuWare users.

Users can incorporate forms into lists (Task Manager) or task lists (Workflow Manager). The system also supports merge forms within workflows for later field completion.

---

## Configuring Forms

**Description:** Create web-based forms with DocuWare Forms. Capture data using various input types and streamline workflows with easy submission and storage.

### Introduction
DocuWare Forms enables creation of web-based forms without coding. The platform supports "text fields, check boxes, drop-downs, calendar inputs, file uploads, and more" for data capture.

Each web form includes configuration settings for fields, indexing, storage location, and access rights. Users access forms via links and submit them as PDFs to file cabinets with a single click. "Submitted forms are stored automatically and are immediately available to all authorized DocuWare users."

Users can incorporate forms into lists (Task Manager) or task lists (Workflow Manager). The system also supports merge forms within workflows for later field completion.

### Prerequisites

Four preliminary requirements exist:

1. **DocuWare Forms functional right** - Users require the "Configure forms" functional right, assignable through DocuWare Configurations > User management.

2. **System storage path setup** - On-premises installations need a temporary storage location configured in DocuWare Administration > DocuWare System > General > System Storage Path. "The specified storage location can be located locally on the server computer or in the network."

3. **Store dialog assignment** - Form administrators must assign store dialogs to authorized users through File cabinets > DocuWare Configurations > File Cabinets > File Cabinet x > Dialogs.

4. **External validation service** - "The validation service allows you to compare the entries in a form with an external data source such as CRM before transmission."

### Configurations Overview

Forms configurations appear in the overview page "in order of their creation date." DocuWare generates accessible links for each form automatically.

"Forms can be exported and imported to any DocuWare system running version 6.11 or later."

### Configuration Wizard Tabs

**Designer:** Users "Place the fields that will capture the data on the form. Ten input types are available—text, date, dropdown, and more."

**Submission:** Defines storage method (web form or merge form).

**Output:** Select file cabinet and store dialog for data archival.

**Indexing:** Assign captured data to DocuWare index fields based on selected store dialog.

**Permissions:** Control configuration editing rights and form submission access.

**Supported Versions:** DocuWare Cloud + versions 7.13, 7.12, 7.11, 7.10

---

## Selecting Output Options

"Select a store dialog that will be used for archiving the submitted forms."

The configuration process varies based on submission method, with two pathways:
- **Web form route:** Proceed directly to selecting a file cabinet and storage dialog
- **Merge form route:** First add a form template and map the form, then select the file cabinet and storage dialog

### Select File Cabinet and Store Dialog

Users must choose a store dialog to save completed forms. The associated file cabinet appears in parentheses following the dialog name. The dialog's index fields subsequently facilitate form indexing.

Key note: "The user filling out the form does not see the store dialog. However, he/she must also be assigned the store dialog."

### Define PDF Properties

This section appears only for Merge Form submissions. It covers:
- **Flattened PDF option:** "Generate flattened PDF (non-editable)" prevents post-storage modifications
- **Hidden field visibility:** Administrators control whether hidden field content transfers to form templates; disabled by default for new forms but enabled for existing ones (DocuWare 7.8 and earlier) to maintain upgrade compatibility

### Attachments

Available exclusively for Merge Form submissions with at least one attachment field. Administrators can selectively enable attachment fields, though minimum one must be enabled. "All attachments are enabled by default."

**Supported Versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Adding a Merge Form (Submission with Merge Form)

### Overview
A Merge Form is a DocuWare form type for inserting variable data into pre-existing documents. Rather than storing the web form itself, the system merges entered data into predefined templates and archives the completed documents.

### Key Concepts

**Purpose:** "DocuWare takes the entered data, merges it into one or more predefined templates (PDF, Word, TIFF, JPG, etc.)" When multiple templates exist, separate PDFs are generated for each.

**Requirements:** At least one enabled Merge Form is necessary for web form completion. The system requires the System Storage Path for temporary file storage.

### Creation Process

Steps for building a merge form:

1. Access the Merge Forms tab after selecting that option in submission settings
2. Add a template in any DocuWare Viewer-supported format
3. Link web form and merge form using fill areas by dragging borders and mapping fields
4. Two mapping methods exist: drag borders then assign fields, or create areas and map directly
5. Note that web form field names don't automatically transfer to merge forms

### Fill Area Settings

- **Fill Mode:** Defines how merge form areas populate based on web form field types
- **Field Content:** Auto-transfers from text/number fields; handles checkboxes and lists
- **Mark with 'X':** Designates selection buttons with an X
- **FixedValue:** Alternative marking symbol to X
- **Font:** Formatting options including size, color, weight, direction
- **Sample Text:** Preview text displayed in fill areas (unsaved)
- **Wrap Text:** Splits single-line text across multiple lines (default on for new forms since 7.10)
- **Fill Area Name:** Auto-assigned from linked fields or custom entry
- **Mapped Field ID:** Unique assignment to web form fields

### Practical Tips

- Assign single fields to multiple fill areas for repeated data
- Use Ctrl+click to edit multiple areas simultaneously
- Right-click for common functions within the designer
- Employ keyboard shortcuts (Ctrl+A select all, Ctrl+Z undo)
- Copy, cut, paste fill areas between forms
- Remove mappings via Edit tool → Show All Mappings → trash icon
- Use "View whole page" for complete overview
- Employ sample text to verify text positioning, especially with wrap text enabled

### Workflow Integration

"You can embed an empty form field into a workflow and have it filled out directly in the mask of a workflow task." Create blank fields by dragging fill areas without mapping them to web form fields.

### Best Practice: Order Forms

DocuWare 7.8+ introduced control over transferring hidden field content to merge forms. This supports streamlined ordering:

1. Create template-matching fields with zero pre-values for calculations
2. Implement behaviors to hide unneeded rows based on submitter quantity selection
3. Uncheck "Show values from hidden fields" option (unchecked by default in new forms)
4. Set editable PDF formatting if future modifications are needed

**Supported Versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Indexing Forms

Data entered in forms populates DocuWare index fields. The Indexing tab in form configuration maps index fields from the store dialog to form fields. Mandatory index fields must be completed before submission. Read-only fields don't appear in the indexing interface.

### Fill Mode Options

**Web Form Field Method:**
This approach connects index fields to form inputs. The Value dropdown adjusts based on field type:
- "Number" type index fields exclude text elements
- "Checkbox" form fields work with keyword index fields
- "Decimal number" file cabinet fields match "Number" form fields
- "Date/Time" file cabinet fields match "Date" form fields

"When you link a form field File attachment to an index field, the name of the attached file (with extension) is entered as an index value."

File attachments save as original-format DocuWare documents. Multiple attachments separate filenames with semicolons. Tables require matching index tables. The guidance suggests matching field types and names between forms and index tables, then using "Assign columns" for automatic alignment.

**Fixed Value Method:**
Users enter static text that automatically fills index fields. This enables quick document retrieval using consistent identifiers like "Document type: Form." Select list options appear as available entries when restriction settings apply.

**Important Note:** "The document name of the stored form in DocuWare does not necessarily correspond to the title of the form."

**Supported Versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Forms Permissions

"The last step in setting up a form is assigning permissions."

### Permission Types
Two distinct permissions exist:

**Use Permission:** Allows individuals to complete and submit forms.

**Manage Permission:** Enables modification or removal of configuration settings. Using the form also requires the Use permission.

### Assignment Methods
Permissions can be granted to specific individuals or through role-based group assignments. Role-based assignment offers advantages, as new staff members automatically inherit user rights when assigned to a particular role.

### Public Form Functionality
Forms can be released for public access, allowing external users to complete and transmit them to DocuWare without direct system access. This requires storing credentials for a designated DocuWare user who will receive the submitted forms. User accounts can be established through DocuWare Administration or Configuration tools. The specified public user must possess access rights to the output storage location.

"For Public Forms no Client License is required for the transmission and archiving of the completed form."

### Sharing via Link
Once configured, the system generates a shareable link for the Web Form, visible on the Overview page. This link enables distribution through email or other communication channels.

**Supported Versions:** DocuWare Cloud, versions 7.13, 7.12, 7.11, and 7.10

---

## Designing Forms (Forms Designer)

To design forms, navigate to DocuWare Configurations > Capture > Forms. Create new or open existing forms, then click the Designer tab.

### Adding Fields to Forms

**Initial Setup:** First establish a form name (internal use only, not visible to users).

**Insertion Methods:** Double-click form fields on the left sidebar or drag them to the center area. Fields are freely positionable with adjustable length and width. Horizontal arrangement is supported, and a stored grid assists with coordinate alignment. Adjacently arranged fields stack vertically on smartphones.

**Preview Function:** Shows browser and mobile device renderings. File attachments cannot be tested in preview.

**Performance Recommendation:** "Limit each form to ca. 100 fields" to maintain performance.

### Form Fields Overview

**Input Fields:**
- Single line text
- Multiple line text (height-limited lines)
- Number field
- Date (with date selector)
- Checkbox (multiple selections)
- Multiple choice (single selection)
- Drop Down (selection list)
- Table (up to 12 columns per table; supports single line text, numeric, date, dropdown formats; maximum 200 rows; not supported for merge forms)
- File attachment (configurable file types and quantities)
- Signature (mouse or touchscreen input)

**Fixed Elements:**
- Title (displayed as form name to users)
- Fixed text (headers, labels)
- Image (maximum 5 MB; PNG or JPG recommended; not displayed when merged with Web Forms)
- Automatic number (unique, consecutive numbering)
- Space (empty field, excludes mobile view)

### Field Settings

- Field IDs are auto-generated from field names plus numbers, distinguishing similar fields
- Default font is Tahoma
- Mandatory fields display asterisks (*)

**Text Fields:** Field masks in single-line text fields enforce correct formatting. "The form will not be submitted until the inputs match the mask definition." All organizational field masks are available.

**Fields with Lists:**
- Multiple choice, checkboxes, and dropdown lists have unlimited select options
- Options sort ascending or descending
- Multiple selection options can arrange horizontally for simultaneous visibility
- Single-column select lists can populate dropdown selections

**Tables:**
- Four field types supported (single line text, numeric, date, dropdown) up to 12 columns
- Equal automatic width distribution applies
- Maximum 200 rows per table
- "Show total" option (numeric columns only) automatically sums entered numbers

**File Attachment:**
Default permitted types: ".pdf, .doc, .docx, .jpg, .jpeg, .gif, .png, .bmp, .tif, .psd, .xls, .xlsx, .txt, .mp3, .mp4, .aac, .wav, .wmv, .avi, .mpg, .mpeg, .zip"

Limitations:
- Combined attachments: maximum 20 MB
- Single attachment: maximum 10 MB
- Maximum 10 files per field

### Calculations
Combine number fields and fixed values using: addition/subtraction, multiplication/division, fixed values, brackets, and percentage calculations (DocuWare 7.11+).

### Behavior
Fields display conditionally or alter properties (Write-protected, Required status) based on user input.

### Predefined Field Entries
Pre-populate fields (current date, logged user name/email) for simplified form completion, customizable during submission.

### Field Validation
"The entries in form fields can be checked for consistency before sending." Submissions require matching defined specifications or field-to-field consistency.

**Version Note:** "With DocuWare 7.13 or later, a 'number equals dropdown' rule fails if the number field and the select list option use different formats, e.g., 2,000 versus 2000."

### Form Properties
Minimum browser width: 600 pixels. Background color customizable via color picker or hexadecimal values. Mobile devices generate single-column views.

**Supported Versions:** DocuWare Cloud + 7.13 + 7.12 + 7.11 + 7.10

---

## Submitting Forms

"DocuWare Forms are web-based forms that capture data and store it directly in a DocuWare file cabinet."

**Configuration Path:** DocuWare Configurations > Capture > Forms > Submission

### Document Type

**Web Form:** The completed form converts to a PDF file that mirrors the Forms Designer layout.

**Merge Form:** Used when a finished template exists (contract, application, government PDF). Users map web form fields to template locations. Upon submission, DocuWare "merges" the data into the template and saves the completed document.

### Post Submission Options
- Display "Start a new form" button
- Show link to submitted form in DocuWare
- Trigger automated actions (URL redirects)

### Pre-fill Feature (DocuWare 7.13+)

Enables users to partially complete forms, save progress, and return later for submission. Process owners can pre-fill and send forms to designated users. Applies to both private and public forms.

**Enabling Pre-fill:** Navigate to DocuWare Configurations > Capture > Forms > Forms configuration xxx > Submission. Activate "Allow the form to be pre-filled."

**Saving Unfinished Forms:** Enable "Allow the form to be pre-filled" and "Show 'Copy form link' button."

**Limitation:** "Data provided in table fields, attachment files, and signature fields cannot be saved with this feature."

### Manual URL Pre-filling
Basic pattern: **Organization Domain/docuware/formsweb/Forms Name?orgID=Org ID**
Example pre-filled link: **/DocuWare/formsweb/Form-Name#pf=on&SingleLineText=Hello**

#### Supported Field Types for Pre-filling
- **Single-line/Multi-line text:** Use URL encoded values
- **Number:** Use invariant format (no thousands separator, dot for decimals; example: 123456.789)
- **Date:** ISO UTC format (example: 2025-06-29T21:00:00.000Z)
- **Dropdown/Radio:** Pass selected option text, URL encoded
- **Checkbox:** Multiple selections require individual specification connected with "&"

**Supported Versions:** DocuWare Cloud + 7.13 + 7.12 + 7.11 + 7.10

---

## How-to: Send a Pre-filled Form as a Workflow Task (Automated Form Pre-filling)

### Introduction
Use workflows to automate form pre-filling with index data and distribute the pre-filled form as a task to assignees for completion.

### Example Scenario
A purchase order request form with "Requestor" and "Date" fields pre-filled and read-only. Goal: Pre-fill "Supplier" and "Project" fields with workflow-collected values. Decision makers complete "Cost Center" and "Contact" fields.

### Workflow Setup Instructions

**Step 1: Create Global Variable**
Create a new global variable (e.g., "PFFormURL") for the destination in the Assign data activity.

**Step 2: Add Assign Data Activity**
- Set Destination type to Global Variable
- Set Source type to Expression
- Build the URL expression using Organization Domain + form URL + pre-fill parameters

**Expression Pattern:** "/formsweb/name-of-your-form#pf=on"
Use ConvertToURLString function: "Supplier=" & ConvertToURLString(Company)

**Step 3: Add Task Activity**
- Choose Method > Dialog
- Add a Decision with a Link field
- Set Predefined type > Global variable pointing to PFFormURL

### Best Practice
Set fields to read-only via the checkbox in field settings. This allows removal of those sections from the expression, and values won't appear in the URL at all.

**Supported Versions:** DocuWare Cloud

---

## Introduction to Workflow Designer as Desktop App

### Overview
Workflow Manager executes previously created configurations, with each run generating a new workflow instance. Tasks can be assigned to users, roles, or substitution rules. Substitution rules handle abstract responsibilities, automatically routing to the first available person. Escalation levels establish deadlines and determine actions when tasks remain unprocessed too long.

Rights management encompasses designer and controller roles. Controllers monitor open participant tasks, while designers can additionally create, modify, and delete workflows.

The complete Workflow Manager is included with every DocuWare Cloud license. For locally installed systems, it's available as an add-on module.

### Installing Workflow Designer
"Workflow Designer is a desktop app that is installed locally on the PC." Access the installation wizard through DocuWare Client's main menu under Install Desktop Apps.

### Configuring Workflows

**Trigger**: "You specify which event generates a new workflow instance." Includes new documents or modified index words. Workflows can also trigger via schedule, with a maximum of 100 documents per schedule.

**Tasks**: Define tasks and assign them to users, roles, or substitution rules.

**Decisions**: "You specify which decision options within a task are given to the responsible user."

**Reminders**: Timing for user reminders and task reassignment via timeout.

**Connections**: Access to external data sources while documents pass through workflows.

### Processing Tasks in DocuWare Client

The workflow tasks area comprises:
- Navigation bar and menu at top
- Task list in center
- Decision area at bottom

**Workflow history**: "The workflow history displays which decisions have been made by which users when processing a workflow." In DocuWare Version 7.12, users need Search or Display Document file cabinet permissions.

**Reassign function**: Can be activated or deactivated per workflow (activated by default).

### Send Request from DocuWare Client

"If you only wish to send a short request to colleagues or business partners about a document, the function Send request is ideal." Suited to one-off or infrequent processes where standard workflows would be excessive.

### Best Practice for Workflows

**Index data and variables:** "Workflows are not controlled via index entries in Workflow Manager (unlike the Task Manager module)." "Access to index fields requires significantly more time and resources than does the integration of variables."

**Stamps:** "Workflow history is the best option to track the decisions made in a workflow." Stamps should be used sparingly for performance reasons.

**Email notifications:** "Email notifications are sent individually for every document and every task." Set up notifications only for users who don't work in DocuWare regularly.

**External data and databases:** "the SQL query is defined in such a way that only one result is returned."

**System variables:** "It is advisable to use the 'Task User' variable for assigning to users."

**Functional right "View All Users":** Required for users assigned to Workflow Designer, Workflow Controller, and Workflow System User roles. "The View All Users permission is critical for workflows to function correctly. There is no workaround or alternative configuration available."

**Supported Versions:** DocuWare Cloud + 7.13 + 7.12 + 7.11 + 7.10

---

## Managing Configurations (Workflow Designer Desktop App)

Managing workflow configurations through the Workflow Designer Desktop App. (Page content dynamically rendered.)

---

## Define Activities

An activity represents a workflow segment executing either automatically or via user action. Users create workflows by dragging activities from the sidebar into the flow diagram. Each placed activity opens a configuration window for detailed setup.

When adding activities, the preceding node must connect to the current step using drag-and-drop from the yellow output area.

**Tooltip Information:** Hovering over placed activities displays configuration details:
- "Assign to: list of the assigned users/roles/substitution rules"
- "Task or Parallel task: description of the task and list of decisions"
- "IF ... ELSE: defined condition"

"If an employee is to make a decision, the assignment must be made beforehand using the Assign to activity."

Activities require unique names within each workflow.

**Supported Versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Assign To - Activities

This activity "assign[s] the next workflow task to specific substitution rules, users, roles, and variables."

### Assignment Options
- Task assignment via substitution rule
- Direct assignment to individual users
- Role-based assignment to all users holding that role
- Assignment using a variable

When selecting the Variable option, the system displays "all variables with a username of type 'User,' 'Role,' or 'Substitution rule' of your DocuWare organization."

If Task or Parallel Task serves as the initial activity without prior person assignment through Assign to, "the task is assigned to the user who triggered the workflow or workflow instance—for example, by storing a document."

**Supported Versions:** DocuWare Cloud + 7.13 + 7.12 + 7.11 + 7.10

---

## Task - Activities

Task activities define workflow tasks assigned to users. (Page content dynamically rendered.)

---

## Parallel Task - Activities

"A parallel task consists of several identical tasks, which need to be performed in parallel by different employees before the workflow is continued with the next step."

### Configuration Sections

**General**: Configure basic parallel task properties.

**Notification**: Email notifications inform users of new assignments.

**Decisions**: Define user decisions with:
- General decision properties
- Dialog fields for data entry
- Input validation rules
- Document stamping options (e.g., "approved")
- Data assignment from source to destination

**Assign To**: "In contrast to a usual task, this is done in just one step for a parallel task."

**Escalation Levels**: Two reminder and due date escalation levels can be configured.

**Termination Conditions**: "Termination can be useful if several users should accept partial amounts of an invoice, but one of these users accepts the whole amount." Administrators enter Visual Basic expressions to stop tasks when specified criteria are met.

**Supported Versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Assigning Data - Activities

The Assigning Data activity enables workflows to "read data directly from a source and writes it into a defined destination," facilitating automated steps without user intervention.

### Destination Types

| Type | Function |
|------|----------|
| Fill area on document | Workflow activity writes value to form |
| Document index data | Indexes or modifies document index information |
| Workflow global variable | Populates values for multi-step workflow use |
| File cabinet | Modifies index data via SQL specification |
| Index table – multiple columns | Adds or replaces index table content |
| Index table – single column | Adds or replaces column content row-by-row |

### Entry Types (Data Sources)

| Type | Purpose |
|------|---------|
| Fixed entry | Writes static values |
| Workflow system variable | Transfers system-generated data |
| Workflow global variable | Transfers variable values |
| Arithmetic expression | Writes computed or combined values |
| Document index entry | Transfers document index data |
| Locale data connection/External data | Writes data from an external source |
| File cabinet | Transfers data between file cabinets |
| Index table | Transfers table data |

### Index Table Data Management

**Full Table Transfer:** Select "Index table > Multiple columns" as destination. When Replace is enabled, "all existing rows in the destination table will be removed and replaced with new rows." Otherwise rows are appended.

**Individual Value Transfer (Match Code):** Enable "Compile rows by match code" to selectively transfer values based on criteria. "Replace option is always enabled for compiling columns by match code."

**Single Column Editing:** Use "IndexTable – Single Column" to copy or replace individual column data.

### Arithmetic Expressions

"Arithmetic expressions are expressions from Visual Basic for Applications (VBA) and .NET as well as specific DocuWare customizations."

**SYS_ROW_NUMBER Column:** Returns the current row number (starting at 1). Indexers count from 0, while "SYS_ROW_NUMBER" starts at 1 — subtract 1 when needed.

### Date Variables
"The date must be defined according to one of the following notations: cdate("YYYY/MM/DD"), cdate("YYYY-MM-DD"), cdate("YYYY.MM.DD")"

**Supported Versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Condition - Activities

Conditional logic activity. Example: "a user has accepted an invoice and must enter its amount. A condition should then be used to check whether the amount is greater than the number 1000."

### Three Configuration Elements:

1. **Condition**: "Enter the condition with a Visual Basic expression, either directly into the field or using the Arithmetic Expression dialog."
2. **Condition fulfilled**: "Select the color to represent the Then command in the flow diagram from the dropdown list and give the Then command a name."
3. **Condition not fulfilled**: "Select the color to represent the Else command in the flow diagram from the dropdown list."

**Supported Versions:** DocuWare Cloud + 7.13 + 7.12 + 7.11 + 7.10

---

## Email - Activities

The Email activity notifies employees about new workflow tasks via email, particularly useful for staff who don't frequently access their task list.

### Email Configuration
- **Recipients:** Select through variables — users, roles, or global variables
- **Subject Field:** Enter subject using variables or index fields. Example: "Workflow [invoices]: You have been allocated a new task"
- **Body Field:** Input email text supplemented with document links, system variables, or index fields

**Supported Versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Web Service - Activities

The Web Service activity integrates REST or SOAP web services into workflows, enabling automatic data exchange between systems. "Web services can be used to automatically exchange data between systems or to create, update, or delete information in other applications via workflow."

### Configuration

1. **General:** Select REST web services with JSON or XML data formats. OpenAPI specification files can be imported to auto-populate available endpoints.

2. **Request:** Select HTTP method, configure URL with path/query parameters, structure HTTP body content. Test requests via "Send" button.

   **HTTP Body:** Attach current documents to external RESTful services. Documents can be exported as original files or PDFs without annotations. "If the DocuWare document contains multiple files (clipped), all files are exported and attached separately."

   **Encoding Options:**
   - Encode special characters (recommended)
   - Encode special characters except reserved URL characters
   - Do not encode special characters

3. **Data Assign:** Assign response values to global variables or index data. "If you aim to handle all returned entries, manually replace the index with an asterisk (*) in the array indexer."

### Default Web Service: DocuWare Platform API

Provides access to file cabinets and documents. Available endpoints include:

- Get total amount of documents (POST)
- Search by dialog (POST)
- Create new database entry (POST)
- Get/Delete document (GET/DELETE)
- Add stamp — automatic or fixed position (POST)
- Add text annotation (POST)
- Transfer document (POST)
- Replace file / Append new file (POST)
- Merge layers / Append document (PUT)
- Create/Modify user (POST/PATCH)
- Get all users / users by group/role (GET)
- Add/Remove user to/from role or group (PUT)
- Get all roles/groups (GET)

**Supported Versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Wait for Event - Activities

This activity enables workflows to pause and wait for documents related to a task to arrive or be processed. Documents can be stored in any file cabinet within the system.

### Configuration:
1. Select the file cabinet where the expected event will occur
2. Define conditions using the same method as trigger conditions
3. Set the number of days to wait for the event
4. Designers can optionally continue running the instance via the context menu

**Supported Versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Time Delay - Activities

This activity establishes a fixed waiting period for workflow instances.

### Use Cases
1. **Resubmission** - Enables staff to create self-assigned workflow resubmission tasks
2. **Time loop** - Permits web service checks with scheduled repetition
3. **Technical necessity** - Pauses workflows while awaiting external system responses

### Configuration
Users can specify duration in days, hours, or minutes through the dialog interface or a date/time variable.

**Limitation:** "The maximum waiting time is 365 days."

**Supported Versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Workflow Analytics API

The Workflow Analytics API enables workflow data integration for analytics tools like Microsoft Power BI. Available for DocuWare Cloud and on-premises installations (version 7.13+).

### On-Premises Paths:
- Physical: `Program Files\DocuWare\Web\WorkflowAnalyticsService`
- Virtual (IIS): `{organization domain}/DocuWare/Workflow/Analytics`

### Key Features
- Analytics for process optimization and bottleneck identification
- JSON and CSV data formats
- 90 days of data persistence
- Automatic 24-hour updates
- Efficient handling of large datasets

### API Structure
Two main endpoint categories: Analytics Configuration (verify, activate, deactivate data projections) and Workflow Analytics (retrieve projection data).

**Swagger Access:** `https://[your].docuware.cloud/DocuWare/Workflow/Analytics/index.html`

### Authentication & Authorization
Access requires OAuth2 Bearer Token authentication. Users need Designer or Controller workflow roles.

### Data Projection Types

| Type | Function |
|------|----------|
| TaskExecutionTimes | Task duration metrics |
| TaskDecisions | Decision choices with timestamps |
| TaskDecisionUsers | User decision attribution |
| TaskFormFieldsData | Submitted form data |
| TaskReactionTimes | Task pickup duration |
| WorkflowErrorExits | Error exit tracking |
| WorkflowRuntimes | Instance duration and status |
| WorkflowGlobalVariablesChanges | Variable data changes |

### API Endpoints

**Enable Data Projections:** `POST /DocuWare/Workflow/Analytics/Configuration/v1/EnableProjections`

**Check Enabled Projections:** `GET /DocuWare/Workflow/Analytics/Configuration/v1`

**Retrieve Projection Data:** `GET /DocuWare/Workflow/Analytics/v1/{workflowId}/[ProjectionType]`

**Supported Versions:** DocuWare Cloud and 7.13

---

## Three-Way Match Workflow Configuration

This workflow "checks invoices against two other documents, such as the delivery note and the purchase order."

### Prerequisites

**Required Documents:** Purchase order, delivery note, and invoice — all with document numbers and line items in index tables.

**Required Database Fields:**
- Document Type, Document Number, Order Number, Status (Text)
- Line Items table: ID, Name, Quantity, Unit Price, Amount (Decimal)
- Matching fields: PO Unit Price, PO Quantity, DN Quantity, Amount Deviation, Quantity Deviation (Decimal), Match Status (Text)

### Configuration Steps

**Step I:** Define Trigger — activates when a new invoice is stored.

**Step II:** Create Activity for Retrieving Order Number — create global variable "GV_myPONumber" and "Assign Data" activity.

**Step III:** Configure Matching Activities (8 lines):
1. Retrieve Purchase Order Data using matchcode on Line Items[ID]
2. Calculate Amount Matching: `DW_LINE_ITEMS[LINE__LINE_AMOUNT]-(DW_LINE_ITEMS[LINE__PO_QUANTITY]*DW_LINE_ITEMS[LINE__PO_UNIT_PRICE])`
3. Retrieve Delivery Note Quantity
4. Compare Quantities across all three documents
5-7. Derive Match Status: "✓ OK", "Amount Deviation!", or "Quantity Deviation!"
8. Set Document Status to "Review" when discrepancies detected

**Step IV:** Evaluation with Condition: `Count(Filter(DW_LINE_ITEMS[LINE__MATCH_STATUS], "Amount Deviation!")) = 0 AND Count(Filter(DW_LINE_ITEMS[LINE__MATCH_STATUS], "Quantity Deviation!")) = 0`

- Non-matching: route to "Review Invoice" task
- Matching: route to "Approved" status

Requires DocuWare Workflow Manager version 7.8+.

**Supported Versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Examples for Workflow Configuration

(Category page — links to specific workflow configuration examples.)

---

## Workflow Manager: Supported SQL Operators and Functions in WHERE Clause

"The SQL WHERE clause is used to filter records based on specified conditions."

### Standard SQL Operators

**Comparison:** = != <> > < >= <=
**Logical:** AND, OR, NOT
**Range:** BETWEEN
**Set:** IN
**Pattern Matching:** LIKE with % and _ wildcards
**Null:** IS NULL, IS NOT NULL

### Standard SQL Functions

**String Functions:** CONCAT, LEN/LENGTH, UPPER/LOWER, TRIM, REPLACE, SUBSTRING, POSITION, CHAR_LENGTH, RTRIM, LTRIM

**Numeric Functions:** ABS, ROUND, CEIL/CEILING, FLOOR, MOD/%, POWER, SQRT

**Date/Time Functions:** GETDATE/CURRENT_DATE, CURRENT_TIME, CURRENT_TIMESTAMP, DATEPART/EXTRACT, DATEADD/ADDDATE, DATEDIFF, FORMAT/DATE_FORMAT

**Aggregate Functions:** COUNT, SUM, AVG, MIN, MAX, GROUP_CONCAT

**Conditional Functions:** CASE WHEN, COALESCE, NULLIF

**Conversion Functions:** CAST, CONVERT

### Subqueries
Single-row and multi-row subqueries are supported.
**Unsupported:** Correlated subqueries, JOIN and APPLY operators in subqueries.

---

## Notifications

Automated email generation triggered by specific events, such as document storage or index value modifications. Example: a cost center manager receiving notification about an invoice requiring approval, with an embedded link enabling direct access within the Viewer.

### Configuring Notifications
"To create or change email notifications, you need the Manage Email Notifications right, which can be assigned in DocuWare Administration under Users/Profiles > Function settings."

"Subscribers can be specified by selecting an Index Field (in the Subscribers tab) in addition to creating a manual entry."

### Licensing
For on-premises deployments, email notifications require a separate DocuWare Task Manager license.

**Supported Versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Document Transfer

"The Transfer module moves or copies large volumes of documents from one on-premises system to another file cabinet."

### Transfer vs. Synchronization

**Synchronization:** Maintains identical status between two file cabinets through regular or scheduled execution, exchanging data bidirectionally.

**Transfer:** Single, one-directional document transfers. Enables version transfers. Utilizes filter queries for selective document specification.

### Access Requirements
- Users need the Transfer functional right
- Source and target file cabinet access required

### File Cabinet Rights

**Source:** Display documents, Search, Delete documents (optional)
**Target:** Display documents, Store, Search

### Key Operational Details
- Document IDs regenerate in target file cabinets
- Table fields assign automatically (identical names and types required)
- "Transfer does not transfer documents that are in the trash bin"
- If deletion option selected, transferred documents move to trash bin

**Supported Versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Electronic Signatures with DocuWare - Introduction

"Electronic signatures ensure the authenticity of digital documents. In simple terms, this involves adding data to the document to prove its authenticity and integrity."

### Security Levels
DocuWare supports multiple security tiers. Simple signatures include document stamps. For advanced and qualified security levels, DocuWare partners with Validated ID and DocuSign.

### Signature Service Interface
The DocuWare Signature Service functions as a web service integrated into workflow activities. Documents move from DocuWare to external signature providers, which verify signer identity and return signed documents with certificates.

### Preconfigured Solution
A ready-made "DocuWare for Electronic Signature" solution exists with pre-established workflows and file cabinets, available for DocuWare systems version 7.4+.

---

## Electronic Signatures with DocuSign - Overview

### DocuWare Signature Service
Functions as "a web service that is integrated into workflow activities." Only supports PDFs — documents are converted as needed. Annotations from original documents don't transfer to the PDF for signing.

**Technical requirements:** DocuWare Workflow Engine access to the web service; SSL encryption mandatory.

### Registration
Requires DocuWare organization registration with the Signature Service. Two subscription options: Demo and Production.

**Service URL:** `https://signature.docuware.cloud/DocuSignSignatureService.svc`
Configuration requires SOAP type selection without authentication.

### Signature Workflow (9 steps)
1. Trigger condition initiates workflow
2. Web service activity submits document information
3. Signature Service fetches document and converts to PDF if necessary
4. Service sends document to DocuSign
5. DocuSign emails user with signing link
6. User reviews and signs using verification methods (access code, SMS, phone, or KBA)
7. DocuSign adds signature and visual representation
8. DocuSign notifies Signature Service
9. Service retrieves signed document and stores in DocuWare

### Signature Placement
- Fixed placement using page numbers and X, Y coordinates in millimeters
- Variable placement using "AnchorText" parameter

### Workflow Activities
- **Assign Data Activity**: Creates global variables for web service parameters
- **Web Service Activity**: Selects signature service and assigns global variables
- **Wait for Event** (optional): Pauses workflow until signing completion

---

## Electronic Signatures with Validated ID - Overview

### DocuWare Signature Service
Functions as "the interface for connecting to an external signature service provider such as Validated ID."

Only supports PDF format. Excludes DocuWare annotations from signed PDFs. SSL required.

### Registration
**Service URL:** `https://signature.docuware.cloud/ViDSignatureService.svc`

Two subscription options: Demo and Production.

### Signature Workflow (9 steps)
1. Trigger condition activates; workflow starts
2. Web service activity submits document information
3. Service fetches document and converts to PDF if necessary
4. Service sends to Validated ID web application
5. Based on signature type:
   - **Remote:** Email link sent to user
   - **Centralized:** User logs into Validated ID portal
   - **Biometric:** Mobile device receives notification
6. User reviews and signs:
   - Remote: TAN from mobile phone
   - Centralized: PIN entry
   - Biometric: Digital pen signature on mobile device
7. Validated ID adds signature and visual representation
8. Validated ID notifies DocuWare Signature Service
9. Service retrieves document and stores in DocuWare

### Post-Signing
- **Signed:** PostSigningAction (ClipBefore, ClipAfter, Replace); StatusFieldName updated with SuccessStatusValue
- **Rejected:** StatusFieldName updated with FailedStatusValue

---

## Electronic Signatures - Licensing

"To use the DocuWare Signature Service with Validated ID or DocuSign, you sign a service contract with one of them."

| Requirement | Cloud | On-Premises |
|---|---|---|
| Signature Service | Included | Add-on license needed |
| Client licenses | Own DocuWare Client license required | Own DocuWare Client license required |
| Further DocuWare licenses | None | Workflow Manager; Valid maintenance contract |
| Signature volume | Purchase from provider or DocuWare (Validated ID) | Purchase from provider or DocuWare (Validated ID) |
| Signature certificate | Purchase additionally | Purchase additionally |

---

## Service Methods and Parameters with DocuSign

### Service Methods

**AddNewDocumentRemote**: Single signer, single location.
**AddNewDocumentMultiSigners**: Multiple signers, ordered or parallel.
**AddNewDocumentMultiPositions**: One signer, multiple locations.
**AddNewClippedDocument**: Multiple file sections, single document.
**DeleteUnsignedDocuments**: Retract unsigned documents.

### Key Parameters

- **Authentication**: RecipientAuthenticationType (None, AccessCode, Phone, SMS, KBA)
- **Document Details**: DocId, FileCabinetId, SectionNumber
- **Signer Information**: SignerName, SignerEmail, PhoneNumber
- **Signature Placement**: AnchorText, PageNumber, PositionX/Y (millimeters)
- **Status Tracking**: StatusFieldName, SuccessStatusValue, FailureStatusValue
- **Post-Signing**: PostSigningAction (ClipBefore, ClipAfter, Replace)
- **Token**: Customer organization identification
- **Expiration**: DaysBeforeExpiration
- **Report**: IncludeReport, ReportLanguage (13 variants supported)

### Multi-Signer Parameters
- MultiSignerName, MultiSignerEmail, MultiSignerPhoneNumber
- MultiValueSeparator (comma, caret, or pipe)
- OrderedSignature (true for sequential, false for parallel)
- MultiAnchorText, MultiPageNumber, MultiPositionX/Y

---

## Service Methods and Parameters with Validated ID

### Centralized Signature Methods
- **AddNewDocument**: Single signer, centralized signing with PIN
- **AddNewDocumentMultiPositions**: One signer, multiple locations
- **AddNewClippedDocumentCentralized**: Multiple files, batch processing

### Remote Signature Methods
- **AddNewDocumentRemote**: Single signer via email link + SMS TAN
- **AddNewDocumentMultiRemote**: Multiple signers, single document
- **AddNewDocumentMultiPositionsRemote**: One signer, multiple locations
- **AddNewClippedDocumentRemote**: Multiple files, single OTP

### Biometric Signature Methods
- **AddNewDocumentBiometric**: Tablet-based biometric signing
- **AddNewDocumentMultiPositionsBiometric**: Multiple locations
- **AddNewClippedDocumentBiometric**: Multiple files, batch processing

### Additional Methods
- **AddNewDocumentStamp**: Automatic signature certifying authenticity without user action
- **DeleteUnsignedDocuments**: Withdraw documents before signing

### Key Parameters
- DocId, FileCabinetId, SignerName, SignerEmail, Token
- StatusFieldName, SuccessStatusValue, FailureStatusValue
- DateSignedFieldName, DaysBeforeExpiration
- PostSigningAction (ClipBefore, ClipAfter, Replace)
- AnchorText, PageNumber, PositionX/Y, SizeX/Y (millimeters)
- EmailLanguage (br, ca, de, en, es, eu, fi, fr, gl, hu, it, nl, no, pl, pt, ro, zh)
- DeviceName, Language (biometric)
- CertificateGUI, CertificatePin (stamp)
- ReminderFrequencyHours, ReminderMaxRetries (remote)

---

## Workflow Manager Overview

Workflow Manager establishes "clear rules for document handling in your company" through document-based workflows.

### Key Components

**Workflow Designer**: Available in two formats:
- Web-based version (new) - CloudOnly
- Desktop application version (previous version)

**Workflow tasks**: User-assigned tasks appear in the DocuWare Web Client's workflow task list.

**Supported Versions:** DocuWare Cloud + 7.13 + 7.12 + 7.11 + 7.10

---

## DocuWare Request - General

"Create important documents in a standalone digital file cabinet. With the integrated browser, external service providers or customers can search and view documents – without DocuWare or other additional software."

### Application Example
"In the case of a financial audit, for example, you compile all the relevant documents for a fiscal year, export them to a Request file cabinet and hand it to the auditor on a USB stick."

### Default Settings

**Functional Rights:** Users need the Configure Request functional right.

**File Cabinet Rights:** Export requires "Search and Display documents" rights. Import demands File cabinet owner profile.

**Web Client Display:** Export function must be visible in result list options.

### Technical Requirements
"From DocuWare Version 6.12, only Request file cabinets can be imported that were created with DocuWare Version 6.12 or later."

"A Request file cabinet can be created with any DocuWare license. No DocuWare license is required to access documents in a standalone Request file cabinet."

### On-Premises
Requires central storage accessible via UNC connections or FTP servers. FTP syntax: "ftp://adminName:adminPassword@server-name/subdir/"

**Supported Versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## DocuWare Request - Configuration

### Exporting Documents

A standalone Request file cabinet stores document selections, formats, search options, and export schedules.

**Export Methods:** Direct from DocuWare Client lists using "Export as Request" or through the Request module in DocuWare Configuration.

**Key Details:**
- Only documents accessible to executing users are exported
- Table fields export but don't display in Request client
- Document versions transfer when supported
- Workflow histories from current workflows transfer
- Default format is original; PDF conversion optionally preserves annotations
- Documents remain read-only
- Full-text search applies when enabled in source file cabinets

### Re-importing Documents

**Key Restriction:** "All documents are imported even if the same documents are already in the file cabinet."

**Import Limitations:**
- Documents reject if index fields have restrictions that imported documents violate
- Only fields existing in target file cabinets transfer
- Workflow histories don't restore
- Versions become individual documents
- PDF-converted documents cannot import
- Table field imports require identical field/column names and types
- Users need "File cabinet owner" rights
- Only DocuWare 6.12+ Request cabinets import

**Supported Versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## Deletion Policies

DocuWare enables automatic deletion of selected documents following a designated retention period.

### Key Information

**Access:** Users need the "Configure deletion policies permission" in DocuWare Configuration under User Administration.

**Features:**
- A dropdown menu displays all file cabinets accessible to the current user
- Documents locked during policy execution will not be deleted
- Table fields do not appear in the document filter

**Time Zone:** "A deletion policy always displays the time for job execution in the time zone in which the policy was created."

**Supported Versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10
