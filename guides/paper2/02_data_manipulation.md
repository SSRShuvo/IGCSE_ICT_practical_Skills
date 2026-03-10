# Paper 2 Task B — Data Manipulation with Microsoft Access

Microsoft Access is used in Paper 2 for **data manipulation**. You will be given a database file (or asked to create one) and asked to create tables, queries, forms, and reports.

---

## 1. Opening and Saving an Access Database

1. Open Access → **Open** → navigate to the `.accdb` file.
2. Click **Enable Content** if a security warning appears.
3. Save your work frequently with **Ctrl + S**.
4. To save a copy: **File** → **Save As** → type the filename given in the question.

> **Note:** Access saves records automatically when you move to the next record, but you must save design changes manually.

---

## 2. Creating and Modifying Tables

### 2.1 Creating a New Table in Design View
1. **Create** tab → **Table Design**.
2. For each field, enter:
   - **Field Name** — exactly as stated in the question.
   - **Data Type** — see the table below.
   - **Field Properties** (lower panel) — field size, format, validation, etc.
3. Press **Ctrl + S** to save the table; give it the exact name from the question.

### 2.2 Common Data Types

| Data Type | Use |
|---|---|
| Short Text | Names, codes, short strings (set Field Size to limit characters) |
| Long Text | Long descriptions or notes |
| Number | Numeric values (set Field Size: Integer, Long Integer, Single, Double) |
| Date/Time | Dates and times |
| Currency | Monetary values |
| Yes/No | Boolean (true/false) fields |
| AutoNumber | Automatically increments — used for primary keys |
| OLE Object | Files or images stored in the database |
| Calculated | Value computed from other fields |

### 2.3 Setting a Primary Key
1. Click the field row in Design View.
2. **Table Design** tab → **Primary Key** button (or right-click → **Primary Key**).
3. A key icon appears in the row selector.

### 2.4 Adding a Field to an Existing Table
1. Open the table in **Design View** (right-click table → **Design View**).
2. Click an empty row below the last field and enter the field name and data type.
3. Save with **Ctrl + S**.

### 2.5 Deleting a Field
1. Open the table in Design View.
2. Click the row selector (grey box) of the field to delete.
3. Press the **Delete** key → confirm.

### 2.6 Setting Field Properties

| Property | Purpose |
|---|---|
| Field Size | Limits the number of characters (Short Text) or numeric range |
| Format | Controls how the value is displayed (e.g. dd/mm/yyyy for dates) |
| Input Mask | Forces a specific input pattern (e.g. phone number) |
| Caption | Label shown in forms/reports instead of the field name |
| Default Value | Pre-filled value for new records |
| Validation Rule | Expression that data must satisfy (e.g. `>=0`) |
| Validation Text | Error message shown when validation fails |
| Required | Whether the field must have a value |
| Indexed | Speeds up searches; set to **Yes (No Duplicates)** for unique fields |

---

## 3. Entering and Editing Data

### 3.1 Entering Records in Datasheet View
1. Open the table in **Datasheet View**.
2. Click in the bottom empty row and type values in each field.
3. Press **Tab** to move to the next field; the record is saved when you move to the next row.

### 3.2 Editing Records
1. Click the field value you want to change.
2. Edit the value and press **Tab** or **Enter**.

### 3.3 Deleting Records
1. Click the row selector (grey box at the left) to select the record.
2. Press **Delete** → confirm.

---

## 4. Creating Queries

Queries retrieve and display specific records or fields from a table.

### 4.1 Creating a Select Query in Design View
1. **Create** tab → **Query Design**.
2. In the **Show Table** dialog, double-click the table(s) you need → **Close**.
3. In the lower grid (QBE grid):
   - **Field** row: click the drop-down and select a field (or double-click a field in the table at the top).
   - **Sort** row: choose **Ascending** or **Descending** if required.
   - **Show** row: tick the checkbox to show the field in results, untick to hide it.
   - **Criteria** row: enter the filter criteria (see below).
4. **Run** the query: **Query Design** tab → **Run** (red exclamation mark), or press **F5**.
5. Save with **Ctrl + S** using the name given in the question.

### 4.2 Criteria Examples

| Goal | Criteria Example |
|---|---|
| Exact text match | `"London"` |
| Exact number match | `42` |
| Greater than | `>100` |
| Less than or equal | `<=50` |
| Between two values | `Between 10 And 20` |
| Date after | `>#01/01/2023#` |
| Contains text | `Like "*shire*"` |
| Starts with | `Like "A*"` |
| Not equal to | `<>"London"` |
| Multiple criteria (AND) | Enter criteria in the **same Criteria row** |
| Multiple criteria (OR) | Enter one criterion per row in the Criteria grid |
| Yes/No field | `Yes` or `No` |
| Null (empty) | `Is Null` |
| Not null | `Is Not Null` |

> **Common mistake:** Text criteria must be enclosed in double quotes; date criteria must be enclosed in `#` symbols.

### 4.3 Sorting Query Results
- In the **Sort** row of the QBE grid, choose **Ascending** or **Descending** for one or more fields.
- The leftmost sorted field takes priority.

### 4.4 Calculated Fields in Queries
1. In an empty **Field** cell, type: `NewFieldName: [Field1]*[Field2]`
   - Example: `TotalCost: [UnitPrice]*[Quantity]`
2. Access calculates the value for each record.

### 4.5 Aggregate Queries (Totals)
1. In Query Design view, click **Totals** button (**Query Design** tab) — a **Total** row appears.
2. For each field set the **Total** row to: **Group By**, **Sum**, **Avg**, **Count**, **Min**, **Max**, etc.

---

## 5. Creating Forms

Forms provide a user-friendly interface for entering and viewing records.

### 5.1 Creating a Form with the Form Wizard
1. In the **Navigation Pane**, select the table (or query) to base the form on.
2. **Create** tab → **Form Wizard**.
3. Move the required fields from **Available Fields** to **Selected Fields** using the `>` button.
4. Click **Next** → choose a layout (Columnar, Tabular, Datasheet, Justified).
5. Click **Next** → type the form title (use the exact name given in the question).
6. Click **Finish**.

### 5.2 Modifying a Form in Design View
1. Right-click the form in the Navigation Pane → **Design View**.
2. Add/remove/move controls as required.
3. To add a label: **Form Design** tab → **Label** tool → draw and type.
4. To add a text box for a field: **Form Design** tab → **Text Box** → draw, then set the **Control Source** property to the field name.
5. Change colours, fonts, and borders using the **Format** tab.

### 5.3 Form Header and Footer
1. Right-click in the form design area → **Form Header/Footer**.
2. Click in the header or footer section and add a label or image.

### 5.4 Adding a Title to the Form
1. In Design View, click in the **Form Header** section.
2. **Form Design** tab → **Title** button — Access adds a label with the form name.
3. Edit the text if required.

---

## 6. Creating Reports

Reports format and present data for printing.

### 6.1 Creating a Report with the Report Wizard
1. Select the table or query in the Navigation Pane.
2. **Create** tab → **Report Wizard**.
3. Move the required fields to **Selected Fields** → click **Next**.
4. Add grouping levels if required (e.g. group by Region) → click **Next**.
5. Set sort order (up to 4 fields, Ascending or Descending) → click **Next**.
6. Choose layout (Columnar, Tabular, Justified) and orientation → click **Next**.
7. Type the report title (exact name from the question) → click **Finish**.

### 6.2 Modifying a Report in Design View
1. Right-click the report → **Design View**.
2. Sections visible: **Report Header**, **Page Header**, **Detail**, **Page Footer**, **Report Footer**.
3. Move, resize, and format controls by clicking and dragging.
4. Delete unwanted controls by selecting and pressing **Delete**.

### 6.3 Formatting Report Controls
1. Select the control.
2. Use the **Format** tab (background colour, font colour, borders).
3. Resize by dragging the handles.

### 6.4 Adding Calculated Controls to a Report
1. In Design View, add a **Text Box** control in the desired section.
2. Click the text box → set its **Control Source** property to: `=Sum([FieldName])` or `=Count([FieldName])`, etc.
3. Add a label beside it to describe the value.

### 6.5 Grouping and Sorting in a Report
1. **Report Design** tab → **Group & Sort** button.
2. Click **Add a group** or **Add a sort** and choose the field.
3. Expand **More** to set sort order, totals, and header/footer sections for each group.

---

## 7. Relationships

### 7.1 Creating a Relationship Between Tables
1. **Database Tools** tab → **Relationships**.
2. If tables are not shown, click **Show Table** → add the required tables → **Close**.
3. Drag the **primary key** field from one table and drop it onto the matching **foreign key** field in the other table.
4. In the **Edit Relationships** dialog:
   - Check **Enforce Referential Integrity** if required.
   - Choose cascade options if needed.
5. Click **Create**.
6. Save the relationship layout with **Ctrl + S**.

---

## 8. Importing Data

### 8.1 Importing a CSV or Text File into Access
1. **External Data** tab → **New Data Source** → **From File** → **Text File**.
2. Navigate to the .csv or .txt file → **Open**.
3. Choose **Import** or **Link** → click **OK**.
4. Follow the wizard: delimiter, field names in first row, data types → **Finish**.

### 8.2 Importing from Excel
1. **External Data** tab → **New Data Source** → **From File** → **Excel**.
2. Follow the wizard to select the sheet and field settings.

---

## 9. Printing Database Objects

### 9.1 Printing a Table or Query
1. Open the table/query in Datasheet View.
2. **File** → **Print** → **Print Preview** to check layout.
3. Adjust column widths by double-clicking column borders to **AutoFit** if columns are cut off.
4. **File** → **Print** → **Print**.

### 9.2 Printing a Report
1. Open the report.
2. Click **Print Preview** tab to check layout.
3. Adjust margins if needed: **Print Preview** → **Page Setup**.
4. **Print Preview** → **Print** to print.

---

## Common Mistakes to Avoid

| Mistake | How to Avoid |
|---|---|
| Wrong data type for a field | Match data type carefully (e.g. phone numbers are Short Text, not Number) |
| Criteria entered without quotes | Always wrap text criteria in `" "` and dates in `# #` |
| Primary key not set | Always set a primary key on the specified field |
| Fields not shown in query results | Check the **Show** tick box in the QBE grid |
| Report sorted in wrong order | Set sort order in the Report Wizard or in Design View |
| Calculated field formula incorrect | Check field names exactly match (case-insensitive but spelling matters) |
| Saving with wrong name | Copy the exact object name from the question |
