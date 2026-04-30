# DocuWare Web-based Workflow Designer

---

## What's New in the Web-based Workflow Designer

DocuWare has substantially upgraded the Workflow Designer with contemporary features and a refreshed visual design while preserving core functionality focused on user task completion.

Key improvements include:
- **HTML-based architecture**: The new Web-based Workflow Designer aligns with other DocuWare components and integrates directly into DocuWare Configurations
- **Device-independent access**: No longer requires installation on specific hardware; accessible from any location or device
- **Modern interface**: Enhanced usability with improved aesthetic design

### New Features

Compared to the previous Workflow Designer, these enhancements are available:

- **Decision-maker assignment**: Designate decision-makers directly within individual tasks for improved control
- **Action-specific outputs**: Each action independently determines its specific output rather than chaining conditions
- **Automatic saving**: Progress saves automatically, eliminating manual save steps and reducing data loss risks
- **Session management**: Enable tracing, undo, and redo capabilities to recover from unintended modifications
- **Batch operations**: Select multiple actions to copy, paste, duplicate, or delete simultaneously
- **Enhanced shortcuts**: An expanded keyboard shortcut library accelerates workflow design
- **Connector visibility**: Toggle highlighting or hiding of specific connectors—regular, error, or timeout types
- **Error management**: Configure automatic response steps for unexpected workflow interruptions
- **Selective export**: Choose specific workflows to export instead of exporting everything
- **Terminology updates**:
  - "Arithmetic expressions" now called "expressions"
  - "Assign to" activity replaced with "Decision-maker" embedded in task actions

### Removed Functionality
Workflow testing capability has been eliminated from the Web-based Workflow Designer.

### Additional Resources
- Getting started checklist covering requirements and prerequisites
- Dashboard overview describing central page and workflow configuration details
- Step-by-step invoice approval workflow tutorial

**Supported Version:** DocuWare Cloud

---

## Checklist for Getting Started with Workflow Designer

The page introduces a preparatory checklist before creating workflow configurations using the Web-based Workflow Designer. It emphasizes proper permission and settings configuration for smooth operations.

**License Requirements:**
- DocuWare Cloud: License included automatically
- DocuWare On-Premises: "Workflow Manager" license required

### Six-Step Checklist

#### 1. Grant "Design workflows" Permission
Users need this permission to create, edit, or delete workflows. Location: DocuWare Configuration > User Management > User x > Function profiles > Design workflows.

#### 2. Grant "View all users" Functional Right
This functional right is necessary for Workflow Designer, Workflow Controller, and Workflow System User roles. It's also required for all users processing workflow tasks if the workflow's task list includes usernames. Location: DocuWare Configuration > User Management > User x > Function profiles > View all users.

#### 3. Provide File Cabinet Access
Designers need access to the underlying file cabinet. File cabinet access is not cross-checked in Workflow Designer, so assigned designers must independently have proper access. Configuration location: DocuWare Configurations > File cabinets.

#### 4. Set Up Result List
Workflow task list functions inherit from the file cabinet's result list. To enable functions: DocuWare Configurations > File Cabinets > Dialogs > Result > Results List. Users can modify by opening a result list and selecting the "Result list functions option below the field list."

#### 5. Add Fill Areas for Forms
Workflows can populate existing DocuWare forms with automatic values. Forms require fill areas, created through DocuWare Configuration > Forms > Submission with Merge Forms.

#### 6. Draft Your Process First
Users should outline their business process before building the workflow configuration.

### Getting Started Steps

After completing the checklist, users can:
1. Navigate to DocuWare Configurations > Workflow Designer
2. Click "New Workflow" button to access the canvas
3. Define the trigger (start action is pre-configured)

**Supported Version:** DocuWare Cloud

---

## Working with the Workflow Canvas

The workflow canvas serves as the primary workspace in DocuWare's Workflow Designer for creating and editing workflow configurations. Access it via DocuWare Configurations > Collaboration > Workflow Designer > Dashboard, then select "New Workflow" or "Edit."

### 1. Adding Activities, Variables and Checking Errors

**Activities**: Users can add items like Task, Email, and Condition through left-toolbar icons, then configure settings in dialogs.

**List View**: Enables quick navigation to specific workflow items. Clicking an activity in the list repositions the canvas to that element.

**Variables**: Global data placeholders supporting types including Text, Integer, Decimal, Date, DateTime and more.

**Validation**: Red asterisks indicate missing or invalid settings. The system prevents publishing faulty workflows. Clicking error messages allows direct fixes.

### 2. Map Navigation
The canvas accommodates unlimited items. A miniature map highlights the visible area in white, allowing users to click, hold, and drag for navigation across expansive configurations.

### 3. Pan, Undo/Redo and Task Lists

- **Select**: Highlights or moves activity dialogs.
- **Pan**: The hand icon enables canvas movement.
- **Task List**: Shapes the task list appearance in the DocuWare Web Client, allowing column management and result list selection.
- **Permissions**: Assigns designer and controller permissions to users or roles.
- **Copy/Save as Image**: Creates PNG screenshots of entire workflows, excluding toolbars and browser elements.
- **Undo/Redo**: Tracks configuration steps during the current session. Clicking previous steps reverts changes, deleting subsequent steps. Closing workflows clears this history.

### 4. Settings and Publishing

- **Settings**: Toggles connector line visibility and expands/collapses workflow items for better overview in large configurations.
- **State of Configuration**: Automatic saving occurs. The version number reflects the currently opened workflow version. Publishing stores altered configurations as new versions.
- **Publish**: Activates workflows when documents meeting trigger conditions are stored. Only possible when validation detects no errors.

### 5. Switching to Another Workflow
Workflow tabs allow switching between configurations. The arrow icon returns to the Dashboard without closing the current configuration, preserving it for later editing.

### 6. Editing Activities
Each activity type (Task, Condition, Assign data) contains specific settings accessible by clicking the activity to open its configuration dialog.

### FAQ

**Save Location**: Automatic saving eliminates manual save buttons. Undo/Redo panels manage changes. Published workflow alterations create new versions selectable in the dashboard.

**Keyboard Shortcuts**:
- [Ctrl+C]: Copies items with settings, excluding connectors
- [Ctrl+X]: Cuts items
- [Ctrl+V]: Pastes to cursor position
- [Ctrl+D]: Duplicates items
- [Delete]: Removes items
- [Esc]: Cancels paste operations and clears selection

**Finding Activities**: List View displays neatly sorted activities, or the mini map enables zooming and navigation through large configurations.

**Supported Version:** DocuWare Cloud

---

## Managing Configurations (Dashboard)

The workflow dashboard serves as the central hub for creating, editing, and migrating workflow configurations. Access it via DocuWare Configurations > Collaboration > Workflow Designer to view all organizational workflows you have permission to access.

### Selecting a File Cabinet
File cabinets are listed with workflow counts displayed numerically. Clicking a cabinet filters the workflow list to show only those associated with that specific file cabinet.

### Creating and Editing Workflows
**Available filters:**
- Click a file cabinet to view related workflows
- Use the search bar to locate specific workflows
- Apply filtering icons to show new, migrated, or to-be-migrated workflows

**Permission requirements:** Designer permission is necessary for creating new workflows, editing existing ones, or deleting workflows (only when no active instances exist).

### Understanding Workflow Instances
Each start of a published workflow will create a new instance of a workflow. The instances counter shows how many active workflow runs are currently in progress. Performance optimization limits workflow starts to 100 documents per scheduled start.

**Important constraint:** Do not exceed 100 documents in a single workflow instance.

Modifying workflow configurations does not affect ongoing instances. Workflows can only be deleted when all instances are stopped.

### Workflow Naming
Workflow names must be unique organization-wide and appear to users in:
1. The workflow history section
2. The task section

Each workflow receives a unique identifier (GUID) useful for API access.

### Version Management
Editing a workflow automatically creates a new version, preserving development history. Only the current version opens in edit mode, though previous versions can be viewed. The "Edit as version" button allows editing unpublished versions.

**Critical note:** Whenever you edit and save a workflow, a new unpublished version is created. Publish the new version if you want your changes to take effect.

### Export/Import Functionality
Workflows export as JSON files for migration between DocuWare systems.

**Export process:** Select workflows, click Export, specify storage location.

**Import process:**
1. Click Import and select the JSON file
2. For multiple workflows, choose either "Import as new workflow" or "Import as a version of an existing workflow"
3. For existing published workflows, a new version is created automatically
4. For unpublished workflows, the current version is overwritten
5. Enter workflow credentials

### Workflow Migration
The migration feature enables accessing legacy Desktop App workflows in the Web-based Workflow Designer for continued editing and management.

**Supported versions:** DocuWare Cloud

---

## Triggering a Workflow

A trigger activity determines when a workflow should start.

Users navigate to DocuWare Configurations > Collaboration > Workflow Designer, then click New Workflow or Edit an existing workflow to open the canvas. A trigger activates automatically for newly created workflows.

### Two Trigger Types

**1. Document Event Trigger**
This initiates workflows based on document storage or metadata modifications. Three subtypes exist:

- **New document**: Activates when documents are archived (example: invoice storage)
- **Index changes**: Activates when document metadata updates (example: status change from 'New' to 'Approved')
- **New document or index changes**: Combines both scenarios

Users can optionally apply specific criteria before triggering occurs, such as filtering by supplier type.

**Merge Form Enhancement**: Workflows can require documents created via a merge form with fill areas and stored as fillable PDF. This allows populating empty fields during workflow execution. Users need the Use permission in DocuWare Configurations > Capture > Forms.

**2. Schedule Trigger**
Applies identical document event conditions but adds timing requirements. Three scheduling options available:

- Daily or specific days
- Weekly or specific weeks
- Monthly or specific months

### Outputs Configuration
The Outputs section enables conditional document routing to different workflow activities. For example, you may want an invoice with an amount higher than 10,000 to be approved by the head of the department, while other invoices are approved at the team lead level.

**Supported Platform:** DocuWare Cloud

---

## Workflow Activities Overview

An activity represents a workflow step that can route documents, update index data, or request user decisions. Users drag activities onto a canvas, configure properties, connect them in sequence, and publish the resulting configuration.

Activities are located in DocuWare Configurations > Collaboration > Workflow Designer, accessible via the left toolbar within the Canvas interface.

### Activity Descriptions

**Start Activity**
The automatically-generated initial activity where users set the trigger for the workflow and provide the credentials of a workflow user. Configuration includes Permissions, Trigger, and Outputs steps.

**Task Activity**
Assigned to DocuWare users requiring interaction and decisions. Example: invoice approval/rejection. Steps: Method, Decision, Behavior.

**Email Activity**
Notifies any DocuWare user and even employees who have no DocuWare account about updates. Configuration: Method, Errors.

**Parallel Task**
Similar to Task but requires identical tasks to be carried out by multiple employees before proceeding. Example: multi-center invoice approvals.

**Condition**
Automatic decision-making that routes the document in the workflow according to a conditions set. Configuration: Outputs, Errors.

**Assign Data**
Automatically modify the index data of documents stored in DocuWare. Configuration: Data assignment, Errors.

**Web Service**
Exchanges data with external platforms via REST or SOAP protocols.

**Wait for Event**
Pauses workflow pending document or index changes.

**Time Delay**
Establishes fixed waiting periods (maximum 365 days) using days, hours, or minutes.

**Supported versions:** DocuWare Cloud

---

## Routing Documents with Conditions

A condition functions as a workflow mechanism that makes an automated yes/no decision based on the rules you define. These rules examine index data from the current document, typically configured through filter settings. The output is true when one or more rules are satisfied, otherwise false.

### Practical Example
- **True scenario**: The amount of an invoice exceeds €10,000. The invoice is routed to a Senior Manager for approval.
- **False scenario**: The amount is equal or below the threshold of €10,000. The invoice is directed to team level.

### Adding a Condition
Users navigate to DocuWare Configurations > Collaboration > Workflow Designer and select New Workflow or Edit. Two implementation approaches exist:

1. Add a condition as a standalone activity
2. Use trigger or activity outputs to define conditions

Both produce identical results. A meaningful name should be entered, as the condition title will be visible in the Web Client as a part of the workflow history.

### Comparing Implementation Methods

**Condition Activity vs. Conditional Output:**

- **Canvas representation**: Condition activities appear as distinct workflow items, while conditional outputs embed within activity settings
- **Search capability**: Condition activities appear in workflow list view searches
- **Visual clarity**: Multiple activities may benefit from conditional outputs to reduce clutter
- **Chaining**: The condition activity returns a basic 'True' or 'False' output. For both decisions 'True' or 'False', you may chain multiple conditional outputs, which are validated AFTER the first condition has been checked.

### Configuring a Condition

Configuration requires:
1. Clicking Set conditions in the Condition dialog
2. Combining conditions and condition groups

Users can activate the option Advanced query to use expressions to cover more complex use cases.

### Defining Outputs

Every condition has two exit paths: True and False. Output names can be customized—the example suggests using < 10,000 and > 10,000 instead of default labels. The output names are not visible in the Web Client.

**Conditional Outputs Detail**: Multiple subconditions can be added to each True or False path. The workflow evaluates these conditions in sequence: if the first one is met, the document follows that path; if not, the next subcondition is checked immediately.

The evaluation process: The first condition that evaluates to True ends the evaluation and defines the exit. If no subconditions are met, the workflow follows the default path.

### Connecting Outputs
Drag the connector lines from the output port to the input port of another activity.

### Handling Errors

Four error handling options exist:

1. **No error handling** (default)
2. **Restart workflow**: The document is routed through the workflow steps from the beginning again automatically.
3. **End workflow**: The document is routed to the end of the workflow automatically. All changes made up to this point will remain.
4. **Go to step**: Adds an Error output port for manual routing

**Supported Version:** DocuWare Cloud

---

## Using Variables in a Workflow

Variables function as placeholders for specific values which can be re-used multiple times throughout a workflow. They enable dynamic adjustments based on different inputs and conditions, particularly useful for storing document index data, current timestamps, and scheduling automated actions.

The system supports two variable categories: global variables (user-defined) and system variables (pre-set by DocuWare).

### Global Variables

Global variables store specific values across multiple workflow activities. An example demonstrates their use: customer numbers entered in task forms can trigger database lookups that store customer names in variables for subsequent workflow steps. These variables appear in Web Client task lists.

#### Creating Global Variables

Access the Variables icon in the workflow canvas sidebar and follow these steps:

1. Assign a unique identification name (e.g., "MyOrderNumber")
2. Select the variable type:
   - **Text**: Limited to 255 characters
   - **Integer/Decimal Number**: Specify decimal places for decimals
   - **Date/DateTime**: For date-type storage
   - **Keyword**: Stores multiple values without individual selection capability
   - **User, Role, Substitution Rule**: List variables enabling individual value selection

#### Editing Variables

Users can modify variable names while workflows are active without removing prior configurations. Name changes automatically propagate throughout the workflow, including SQL commands. Note: Hyphens are stored internally as double underscores.

### System Variables

DocuWare automatically sets and updates system variables based on type. Examples include the 'last decision user' (continuously updated) and 'Document URL' (static).

#### Complete System Variables Table

| Variable | Function |
|----------|----------|
| Workflow name | Specified workflow identifier |
| Start date/time | Workflow instance initiation timestamp |
| Activity | Current activity name |
| Assigned | User, role, or substitution rule assignment details |
| Last error activity | Error activity identifier |
| Last decision user | User making final decision |
| Last error message | Error type classification |
| Current user | Most recently active editor |
| Task user | Currently active task editor |
| Received on | Task list incorporation date |
| Reminder date | Reminder specification timestamp |
| Pending date | Pending specification timestamp |
| Current date | Present date and time |

### FAQ: Variable Comparison in Conditions

Comparison operators include =, >=, >, <, and <=.

**Date Variables**: Format dates using cdate("YYYY/MM/DD") or alternative notations with hyphens or periods.

**Numeric Variables**: Variables must share identical decimal place counts for comparison. Use the Assigning Data activity to standardize decimal places across variables before conditional evaluation.

---

## How to Connect Workflow Activities

Workflows process documents through sequential steps using activities. Before publishing, all activities require connections to function properly.

### Instructions
Arrange all workflow items in the correct sequence and connect them by dragging a line from the input port of one action to the output port of another.

### Additional Tips
- Connection removal involves selecting it and pressing the Delete key
- For improved clarity in complex workflows, users can hide connector lines or collapse workflow cards

**Supported Version:** DocuWare Cloud

---

## How-to: Reverse and Reapply Workflow Configuration Steps

### Overview
The redo/undo panel enables quick correction of mistakes and reversion to previous states.

### Instructions
Users can access undo/redo functionality by:
- Clicking the Redo and Undo arrows located in the bottom panel
- Clicking the Undo list to view all performed steps
- Selecting a previous step to revert to that stage (all subsequent steps will be deleted)
- Using Redo to reverse the undo action

### Important Limitation
The steps you perform on the workflow canvas are recorded only for the current session. If you close the workflow—by clicking the X in the tab—the configuration history up to that point will not be available the next time you open the workflow.

Users can return to the dashboard without closing the workflow configuration.

**Supported Version:** DocuWare Cloud

---

## How to Validate the Workflow Configuration

A workflow cannot be published until the validation list is empty and no red bullet is visible.

### Validation Process Details

The system performs automatic validation checks to prevent users from publishing faulty workflows unintentionally.

Red indicator bubbles serve two purposes:
- They signal that critical settings require attention
- They can be clicked to navigate directly to the problematic configuration area

### How to Use the Validation Panel

Users should open the validation panel to review any flagged issues. The interface is designed so that selecting an error message takes you directly to the missing setting, streamlining the correction process.

**Supported Version:** DocuWare Cloud

---

## How-to: Invoice Approval Workflow

DocuWare's document-based approval workflow efficiently processes incoming invoices. The basic workflow involves triggering when invoices are stored, routing by amount thresholds, and obtaining approvals or rejections before payment processing.

### Workflow Process Steps

**Initialization:** A new invoice is stored in a DocuWare file cabinet. A new workflow for approval or rejection is executed.

**Amount-Based Routing:** Invoices exceeding 10,000 route to department heads; amounts at or below 10,000 route to team level.

**Approval/Rejection:** Decision makers approve or reject invoices, with approved documents proceeding to payment workflows.

### Configuration Instructions

#### Creating the Workflow
Navigate to Configuration > Collaboration > Workflow Designer, click New Workflow, select the invoice file cabinet, name the workflow, and confirm creation.

#### Start Activity Setup
Requires two elements:
- **Permissions:** A workflow requires a DocuWare user which acts as workflow controller.
- **Trigger:** Select Document event > Type > New document

**Trigger Conditions (two required):**
1. System Index Field "Document ID" IS NOT EMPTY
2. Index field "Document type" equals "Invoice"

#### Condition Configuration
Create a Condition activity with rules:
- **True output:** Amount Greater Than 10000
- **False output:** Amount Less Than Or Equal 10000

Optionally rename outputs (e.g., ">10.000") for clarity.

#### Task Creation (User Group 1)
Create approval task with:
- **Method:** Dialog
- **Decisions:** Two options - "Approve" and "Reject"
- **Fields:** Integer field displaying amount, optional comment text field
- **Data Assignment:** Set status to "Approved" upon approval
- **Decision Makers:** Select users or roles (department heads)

#### Task Creation (User Group 2)
Duplicate the first task and modify:
- Change decision maker to team lead role
- Optionally adjust task colors/names

#### Final Connections
Connect all workflow activity ports using drag-and-drop connectors.

**Supported Version:** DocuWare Cloud

---

## Workflow-Designer: How-to Guides

This is an index/landing page for workflow designer how-to documentation. Content is rendered dynamically and includes links to all the how-to guides listed in other sections.

**Supported Version:** DocuWare Cloud

---

## Assigning Data in a Workflow

The **Assign data** workflow activity enables automatic modification, addition, or removal of index data for documents stored in DocuWare. An example demonstrates how an approved invoice can automatically receive a purchase order number from CRM systems, linking documents for tracking purposes.

### 1. Adding an Assign Data Activity

1. Navigate to DocuWare Configurations > Collaboration > Workflow Designer
2. Create a new workflow or edit an existing one using the canvas interface
3. Select "Assign data" from the left sidebar

Red asterisks appear initially in the configuration dialog, indicating incomplete settings that disappear once all options are configured.

### 2. Configuring Data Assignments

Data assignments require two components: destination (where data goes) and source (where data originates).

#### 2.1 Specifying the Destination

1. Access the "Data" tab within the Action dialog
2. Click "Add first assignment"
3. Select "Set data assignment"
4. Choose a destination type
5. Select a specific destination entry

**Key Notes About Destinations:**
- "Document index," "Global variable," and "Index table" always target workflow document index fields
- "File cabinet" can address both workflow documents and other DocuWare documents
- Each assignment addresses only one index field; multiple assignments are needed for multiple fields
- Destination entry options vary based on selected destination type

#### Destination Types

**Document Index:** Modifies or replaces index values of the current workflow document.

**Global Variable:** Populates a variable whose values can fill workflow document index fields. Variables are reusable across multiple workflow steps.

**Index Table:** Adds or modifies data in workflow document index tables (structured as tables). Users can select table columns, rows, or specific fields for addition or replacement.

**File Cabinet:** Adds or changes index data to documents in any file cabinet. Users write SELECT statements with no SQL skills required—filter settings automatically convert to SQL. Advanced query options support complex use cases with expressions. Important limitation: Only ONE index field per data assignment.

**Fill Area:** Populates merge forms with index data. Prerequisites include merge form selection in workflow trigger conditions. Existing values are overwritten if the fill area links to form fields.

#### 2.2 Specifying the Source

Source type and source entry fields remain inactive until a destination is established.

**Important Distinction:** Source types "Document index," "Index table," and "File cabinet" reference DocuWare-stored index data. However, fixed values, expressions, or variables can also populate destination fields. "Local database connection/External sources" embeds external data. Only entry types matching the destination display.

#### Source Types

**Global Variable:** Adds values from global variables to destinations. Not available for "Index table" destinations.

**Index Table:** Writes data from any DocuWare index table to the workflow document's index table. Exclusively available for "Index table" destinations.

**File Cabinet:** Adds index data from any file cabinet to any stored document's index data. Filter settings convert automatically to SQL.

**Fixed Value:** Adds fixed values to destinations. Values must match destination type requirements.

**System Variable:** Adds values from system-defined variables to destinations. Unavailable for "Index table" destinations.

**Expression:** Enters user-specific values combining different variables into destinations. Users click "Write Expression" to enter expressions.

**Local Database Connection:** Adds values from sources outside DocuWare to destinations. Cloud systems label this "Local database connection"; on-premises systems label it "External source." Installing Local Data Connector in Cloud systems enables rapid synchronization between Cloud and on-premise systems.

### 3. Handling Errors

When automated data assignment fails, workflows can route documents to alternative automated activities.

Error handling configuration occurs in Assign data > Action > Errors tab with four options:

- **No error handling:** Default setting
- **Restart workflow:** Automatically routes documents through all workflow steps from the beginning
- **End workflow:** Automatically routes documents to workflow conclusion while preserving prior changes
- **Go to step:** Adds an "Error" output to the Assign data activity, enabling manual routing

**Supported Version:** DocuWare Cloud

---

## Assigning Data to Index Tables

Updating index tables occurs through the Assign Data workflow activity, which enables adding values or index data from other documents or external systems to a current workflow document's index table, or replacing existing values.

Index tables represent a specialized index field type in DocuWare. To target specific entries, you must identify the correct column and row through filtering.

### Selecting an Index Table as Destination

1. Navigate to DocuWare Configurations > Collaboration > Workflow Designer
2. Click New Workflow or Edit to open an existing workflow in the canvas
3. In the left sidebar, click Assign data
4. Click the links Assign data, Add first assignment, and Set data assignment
5. Choose Destination type: Index table
6. Select an index table from the current workflow document
7. Choose one or multiple columns from the specified index table

### Appending Data to an Index Table

You can append one or more rows to the end of a workflow document's index table, with data sourcing from another DocuWare-stored document.

#### Step 1: Define Source and Assignment Type

1. Select your index table as destination
2. Select all index table columns
3. Choose the Source type:
   - **File cabinet**: for appending another document's index data
   - **Index table**: for addressing an index table stored in DocuWare
4. Activate Append to end of table option
5. Open the assignment wizard

#### Step 2: Specify Index Data to Be Appended

**Choose source:**
- For File cabinet: specify a file cabinet
- For Index table: specify a file cabinet AND an index table field

**Filter source:** Create a rule filtering documents in the selected file cabinet.

**Max. rows returned:**
- File cabinet: Maximum of 1000; default is 100
- Index table: Maximum of 20; default is 1

#### Step 3: Sort the Filtered Source Index Data
Sort the source index data. Index data appends in this sort order.

#### Step 4: Append Data to the Destination Columns
1. Select one source column for each destination column
2. Only map fields that fit together (text to text, not text to date)
3. Click Done

### Replacing Data in an Index Table

When replacing specific values, identify target cells by column and row.

**Source type variations by column count:**
- **One column selected**: Source types Document index and Fixed value become available
- **Multiple columns selected**: Specify source data via File Cabinet or Index table

#### Replacing Specific Values

Replace one specific value with another index value from the current workflow document.

1. Select your index table as destination
2. Activate one Index table column
3. Select Source type > Document Index
4. Choose an index field from the current workflow document
5. Activate Configure row filter option
6. Click Add filter to filter rows
7. Click Done to save and exit

#### Replacing Cells in Multiple Columns or Entire Rows

1. Select your index table as destination
2. Pick columns or Select all for entire rows
3. Choose Source type > Index table
4. Activate Replace existing table data
5. Click Configure table assignment

**Specify source data:**
1. Choose source: Specify a file cabinet and index table
2. Filter source: Create a rule filtering documents
3. Max. rows returned: Index table max 20, File cabinet max 1000

**Filter Destination by Matching Rows:**
- No: ALL rows replace
- Yes: ONLY matching rows replace
- Add conditions to define matches

**Behavior for multiple matches:**
- Process only the first matching row (default)
- Process up to 10 matching rows

**Sort the Filtered Source Index Data**
Sort so required records appear first.

**Filter Destination by Table Columns**
Apply Filter rows in addition to matching rows.

**Replace Data in the Destination Rows**
Map source to destination columns, click Done.

### Index Table FAQ

**What's an Index Table?** An index table is a specialized index field type in DocuWare, allowing storage of multiple values in table format within one index field for a document.

**How Are Index Tables Filtered?** Addressing a specific cell requires: choose the index table, select a column, filter documents, sort data.

**How Are Columns Added?** Column addition occurs in file cabinet configuration.

**How Can I Remove Columns or Rows?** Replace them with empty data using the Assign data function.

**Matching Rows Example:** The matchcode compares columns. If the values in source and destination match, then replacement occurs.

---

## Workflow Expression Parser

The Workflow Expression Parser is a reference documenting which expressions from VBA and .NET you can use in your workflows and how they work with DocuWare-specific customizations. The resource includes examples demonstrating practical applications, such as validating whether variables contain data or remain empty, plus supplementary VBA Expression Examples.

The PDF document is attached to the article and can be downloaded: "Workflow Expression Parser April 2025.pdf"

**Supported versions:** DocuWare Cloud, 7.13, 7.12, 7.11, 7.10

---

## How-to Migrate a Workflow

This guide addresses users transitioning from the Desktop App version to the Web-based Workflow Designer. Users already working exclusively with the web-based designer can disregard this article.

### Migration Overview
The migration feature enables access to all workflows within the web-based Workflow Designer. Legacy workflows from the previous Desktop App version can be migrated to permit ongoing editing.

### Migration Steps

**Step 1:** Access the Web-based Workflow Designer via DocuWare Configurations > Workflow Designer.

**Step 2:** Legacy workflows automatically display in the workflow list. Those requiring migration bear the "TO BE MIGRATED" badge.

**Step 3 - Two Migration Options:**

**Option A - Migrate Button:**
- Migrates the workflow for continued editing
- Creates a new workflow version
- Published versions remain unchanged
- The "TO BE MIGRATED" badge disappears post-migration

**Option B - Create a Migrated Copy:**
- Duplicates the workflow in the Web-based Designer
- Preserves the original in the Desktop App
- Original remains listed with the badge; the duplicate appears as "Workflow (Copy)"

**Step 4 - Version Selection:** The system automatically migrates the published version when available, or the latest draft version when unpublished.

### Filtering Workflows
The top-right filter enables users to categorize workflows by creation and migration status.

### FAQ

**Q: Do I need to migrate workflows?**
A: Yes, if editing in the web-based designer is desired.

**Q: Will migration occur automatically during version 7.13 upgrade?**
A: No automatic migration occurs. Migration is optional unless editing is planned.

**Q: Where are workflows migrated?**
A: Through the "Migrate" option in the Web-based Workflow Designer dashboard.

**Q: How to identify workflows needing migration?**
A: These workflows display a badge and lack an "Edit" button—only a "Migrate" button appears.

**Q: Does migration affect running workflows?**
A: No. Migration creates a new version that activates only upon publication.

**Q: Can multiple workflows migrate simultaneously?**
A: No bulk migration currently exists.

**Q: Can workflows be exported and imported between versions?**
A: No. Exported workflows from the previous version can only be imported back into that same version.

**Q: Can users revert to the Desktop App?**
A: No direct rollback exists. However, users can open workflows in the Desktop App, select an earlier version, and use "Copy and create new version."

**Q: Can multiple workflow versions publish simultaneously?**
A: No. Only one version of a workflow can be published at a time.

**Q: Availability timeline for the Desktop App?**
A: The Desktop App remains available at minimum through version 7.14 (spring 2026), with estimated End of Life in fall 2026 or spring 2027.

**Supported Version:** DocuWare Cloud

---

## Migration Guide: Breaking and Functional Changes

This documentation describes breaking and functional changes when transitioning workflows from the Desktop Workflow Designer to the web-based version.

### Breaking Changes

#### Removal of System Variables

**What Changed:** Five system variables no longer function in web-based activities: WF_ASSIGNED_TO, WF_NOTIFICATION_DATE, WF_EXPIRATION_DATE, WF_LOGGED_IN_USER, WF_RECEIVED_ON. These are automatically removed during migration, becoming NULL values.

**Affected Activities:**
- Email (subject, body, conditional outputs)
- Condition (all query types and outputs)
- Assign data (multiple source types and expressions)
- Web service (SOAP parameters, REST routes, headers, bodies)

**Impact:** Validation failures may occur. Document routing may not function as intended. Variable values are permanently lost.

**Required Actions:** Users must identify activities referencing removed variables and implement alternatives: custom workflow variables, workflow restructuring, or the new "Trigger User" variable.

#### WHERE Clauses in Trigger Conditions

**What Changed:** Desktop Designer allowed typed WHERE clauses after equality operators. Web Designer requires using the query builder instead, with an optional "Is (WHERE clause)" operator.

**Impact:** Imported WHERE clauses appear as plain strings. If unsupported operators exist (like AND, OR, LIKE, CURRENTDATE variants, COUNT, VARIABLE functions), conditions become invalid and read-only.

**Unsupported Operators (Case-sensitive):** AND, OR, NOT, LIKE, CURRENTDATE, CURRENTUSERSHORTNAME, CURRENTUSEREMAIL, COUNT, CURRENT_DAY through CURRENT_YEARMONTH, VARIABLE.

**Unsupported Operators (Case-insensitive):** STARTSWITH, ENDSWITH, CONTAINS, IN, IS EMPTY, NOTEMPTY, PARAMARRAY.

**Symbols:** =, >=, <, <=, <>.

**Required Actions:** Delete invalid conditions. Rebuild using the Query Builder interface. Avoid escape characters. Use the "Is" operator to replicate WHERE clause logic.

### Functional Changes

#### New DecisionMaker Variable
A system-generated, read-only variable automatically replaces the deprecated "Assign To" functionality. All "Assign to" activities convert to "Assign Data" activities.

#### Timeout with Out-of-Office Rerouting
When timeout rerouting is enabled, an additional "Assign Data" activity is automatically created after the timeout exit.

#### Match Codes Sort Order Relocation
Sort settings moved from the "Rows" tab to the "Sort source" tab within the table assignment wizard.

#### Table Column Mapping Changes
Web Designer requires specifying target table columns upfront. Only selected columns are available for subsequent mapping.

#### Email Notification Settings
Notification settings relocated to "Task > Behavior," grouped alongside reminders and escalation options.

#### Fixed-Value Assignments with Missing References
Missing users, roles, or substitution rules trigger removal of associated fixed values. Missing dependencies for file cabinets, web services, or PDFs cause migration failures.

**Supported Version:** DocuWare Cloud
