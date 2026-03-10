# Paper 3 Task A — Spreadsheets with Microsoft Excel

Microsoft Excel is used in Paper 3 for **spreadsheet tasks**. You will be given a data file and asked to enter formulas, create charts, apply formatting, and analyse data.

---

## 1. Opening, Saving, and Navigating

### 1.1 Opening a File
1. **File** → **Open** → navigate to the `.xlsx` or `.csv` file.
2. If opening a `.csv` file, click through the Text Import Wizard or allow Excel to open it automatically.

### 1.2 Saving
- **Ctrl + S** — save in the current format.
- **File** → **Save As** — to rename or change format.
- Use the **exact filename** given in the question.
- If instructed to save as **.csv**, choose **CSV (Comma delimited)** in the **Save as type** list.

### 1.3 Renaming a Worksheet Tab
1. Double-click the tab name at the bottom of the screen.
2. Type the new name (use the exact name given in the question) → press **Enter**.

---

## 2. Entering and Editing Data

### 2.1 Entering Data
1. Click a cell and type the value.
2. Press **Tab** to move right, **Enter** to move down, or arrow keys to move in any direction.

### 2.2 Editing a Cell
- Double-click the cell to edit in-place, or
- Click the cell and edit in the **Formula Bar** at the top.

### 2.3 Deleting Cell Content
- Select the cell(s) and press **Delete** (clears content, keeps formatting).
- To clear everything: **Home** → **Clear** → **Clear All**.

### 2.4 Filling a Series
1. Enter the first value (or first two values for a pattern).
2. Select the cells with the values.
3. Drag the **fill handle** (small green square at the bottom-right corner) down or across.

---

## 3. Cell References and Ranges

| Reference Type | Example | Meaning |
|---|---|---|
| Relative | `A1` | Adjusts when copied |
| Absolute column | `$A1` | Column fixed, row adjusts |
| Absolute row | `A$1` | Row fixed, column adjusts |
| Absolute | `$A$1` | Both fixed — does not adjust when copied |
| Range | `A1:C10` | All cells from A1 to C10 |
| Named range | `Sales` | A named group of cells |

> **Tip:** Press **F4** while editing a cell reference to cycle through relative/absolute options.

---

## 4. Formulas and Functions

All formulas begin with `=`.

### 4.1 Basic Arithmetic

| Operation | Example |
|---|---|
| Addition | `=A1+B1` |
| Subtraction | `=A1-B1` |
| Multiplication | `=A1*B1` |
| Division | `=A1/B1` |
| Percentage of total | `=A1/SUM(A1:A10)*100` |

### 4.2 Commonly Used Functions

| Function | Syntax | Purpose |
|---|---|---|
| SUM | `=SUM(A1:A10)` | Adds all values in a range |
| AVERAGE | `=AVERAGE(A1:A10)` | Mean of values |
| MAX | `=MAX(A1:A10)` | Largest value |
| MIN | `=MIN(A1:A10)` | Smallest value |
| COUNT | `=COUNT(A1:A10)` | Count of numeric values |
| COUNTA | `=COUNTA(A1:A10)` | Count of non-empty cells |
| IF | `=IF(condition, value_if_true, value_if_false)` | Conditional logic |
| SUMIF | `=SUMIF(range, criteria, sum_range)` | Conditional sum |
| COUNTIF | `=COUNTIF(range, criteria)` | Conditional count |
| AVERAGEIF | `=AVERAGEIF(range, criteria, average_range)` | Conditional average |
| VLOOKUP | `=VLOOKUP(lookup_value, table_array, col_index, [range_lookup])` | Vertical table lookup |
| HLOOKUP | `=HLOOKUP(lookup_value, table_array, row_index, [range_lookup])` | Horizontal table lookup |
| ROUND | `=ROUND(A1, 2)` | Round to specified decimal places |
| INT | `=INT(A1)` | Round down to integer |
| LEFT | `=LEFT(A1, 3)` | First n characters of text |
| RIGHT | `=RIGHT(A1, 3)` | Last n characters of text |
| MID | `=MID(A1, 2, 4)` | Characters from position, length |
| LEN | `=LEN(A1)` | Number of characters |
| CONCATENATE / & | `=A1&" "&B1` | Join text strings |
| TODAY | `=TODAY()` | Today's date |
| NOW | `=NOW()` | Current date and time |

### 4.3 IF Function in Detail
```
=IF(logical_test, value_if_true, value_if_false)
```
Examples:
- `=IF(B2>100, "High", "Low")`
- `=IF(C3="Yes", D3*0.9, D3)` — applies a 10% discount if C3 is "Yes"
- Nested IF: `=IF(A1>=90, "A", IF(A1>=70, "B", IF(A1>=50, "C", "F")))`

### 4.4 VLOOKUP in Detail
```
=VLOOKUP(lookup_value, table_array, col_index_num, [range_lookup])
```
- `lookup_value` — the value to search for.
- `table_array` — the range containing the lookup table (use absolute references: `$A$1:$D$20`).
- `col_index_num` — the column number in the table to return (1 = first column).
- `range_lookup` — `FALSE` for exact match (most common in IGCSE), `TRUE` for approximate.

Example: `=VLOOKUP(B2, $F$1:$H$20, 2, FALSE)`

### 4.5 Copying Formulas
1. Click the cell with the formula.
2. Drag the **fill handle** down or across to copy to adjacent cells.
3. Or **Ctrl + C** → select destination range → **Ctrl + V**.

---

## 5. Formatting Cells

### 5.1 Number Formats
1. Select the cell(s).
2. **Home** tab → **Number** group:
   - **Currency** — adds currency symbol, 2 decimal places.
   - **Percentage** — multiplies by 100 and adds `%`.
   - **Comma Style** — adds thousand separators.
   - Increase/Decrease Decimal Places using the `.0` and `.00` buttons.
3. Or right-click → **Format Cells** → **Number** tab for more options.

### 5.2 Date Formats
1. Select the cell(s) with dates.
2. Right-click → **Format Cells** → **Number** tab → **Date** → choose the format.
3. Custom format example: `dd/mm/yyyy` or `d mmm yyyy`.

### 5.3 Text Formatting
- **Bold**: **Ctrl + B** | **Italic**: **Ctrl + I** | **Underline**: **Ctrl + U**.
- Font name and size: **Home** tab → **Font** group.
- Font colour: **Home** → **Font Color** drop-down.

### 5.4 Cell Alignment
- **Home** tab → **Alignment** group: Left, Centre, Right, Top, Middle, Bottom.
- **Wrap Text**: **Home** → **Wrap Text** — text wraps within the cell.
- **Merge and Centre**: Select cells → **Home** → **Merge & Center**.

### 5.5 Cell Background Colour
1. Select the cell(s).
2. **Home** → **Fill Color** drop-down → choose the colour.

### 5.6 Borders
1. Select the cell(s).
2. **Home** → **Borders** drop-down → choose border style, or
3. Right-click → **Format Cells** → **Border** tab for fine control.

### 5.7 Column Width and Row Height
- **AutoFit** column width: Double-click the column border in the column header.
- Manual: Right-click column header → **Column Width** → type exact value.
- Row height: Right-click row number → **Row Height** → type exact value.

---

## 6. Sorting and Filtering

### 6.1 Sorting Data
1. Click any cell in the data range.
2. **Data** tab → **Sort**.
3. Choose the **Sort by** column, **Sort on** (Values), and **Order** (A to Z, Z to A, Smallest to Largest, etc.).
4. Click **Add Level** for multi-level sorting.
5. Click **OK**.

### 6.2 AutoFilter
1. Click any cell in the header row.
2. **Data** tab → **Filter** — drop-down arrows appear on each column header.
3. Click a drop-down → select values to show, or choose **Number Filters** / **Text Filters** for criteria.
4. To remove a filter: click the drop-down → **Clear Filter From…**
5. To remove all filters: **Data** tab → **Filter** (toggle off).

---

## 7. Data Validation

Data validation restricts what values can be entered in a cell.

1. Select the cell(s).
2. **Data** tab → **Data Validation**.
3. On the **Settings** tab:
   - **Allow**: Whole number, Decimal, List, Date, Time, Text length, Custom.
   - Set the **Minimum**, **Maximum**, or **Source** as required.
4. On the **Input Message** tab: add a helpful prompt (optional).
5. On the **Error Alert** tab: choose **Stop**, **Warning**, or **Information** and write an error message.
6. Click **OK**.

**Drop-down list example:**
- Allow: **List** → Source: type values separated by commas (e.g. `Yes,No`) or select a range.

---

## 8. Conditional Formatting

1. Select the cell range.
2. **Home** tab → **Conditional Formatting**.
3. Common options:
   - **Highlight Cells Rules**: Greater Than, Less Than, Between, Equal To, Duplicate Values, etc.
   - **Top/Bottom Rules**: Top 10 items, Above average, etc.
   - **Data Bars**, **Colour Scales**, **Icon Sets** for visual indicators.
4. Set the format (fill colour, font colour, border) → **OK**.
5. To manage rules: **Conditional Formatting** → **Manage Rules**.

---

## 9. Charts

### 9.1 Creating a Chart
1. Select the data range (include labels/headers).
2. **Insert** tab → **Charts** group → click the chart type (Column, Bar, Line, Pie, Scatter, etc.).
3. The chart is inserted on the current sheet.

### 9.2 Choosing the Correct Chart Type

| Chart Type | Best Used For |
|---|---|
| Column | Comparing categories (vertical bars) |
| Bar | Comparing categories (horizontal bars) |
| Line | Trends over time |
| Pie | Parts of a whole (one data series only) |
| Scatter (XY) | Relationship between two numeric variables |

### 9.3 Adding Chart Elements
1. Click the chart to select it.
2. **Chart Design** tab → **Add Chart Element**:
   - **Chart Title** — above chart or centred overlay; type the title.
   - **Axis Titles** — label the X and Y axes.
   - **Data Labels** — show values on bars/points.
   - **Legend** — shows the data series key.
   - **Gridlines** — major/minor horizontal/vertical lines.

### 9.4 Formatting Chart Elements
1. Double-click a chart element to open its **Format** pane on the right.
2. Change fill, border, font, number format, etc.
3. To change the chart colour scheme: **Chart Design** → **Change Colors**.

### 9.5 Changing Chart Type
1. Click the chart → **Chart Design** tab → **Change Chart Type**.
2. Select the new type → **OK**.

### 9.6 Moving a Chart to Its Own Sheet
1. Click the chart → **Chart Design** tab → **Move Chart**.
2. Choose **New sheet** and give it the name from the question → **OK**.

### 9.7 Resizing and Positioning a Chart
- Drag the chart to move it.
- Drag the corner/edge handles to resize.
- For exact size: **Chart Format** tab → **Size** group.

---

## 10. Printing Spreadsheets

### 10.1 Setting the Print Area
1. Select the cell range to print.
2. **Page Layout** tab → **Print Area** → **Set Print Area**.

### 10.2 Page Setup
1. **Page Layout** tab → **Page Setup** dialog launcher.
2. **Page** tab: orientation (Portrait/Landscape), scaling (Fit to 1 page wide by 1 tall).
3. **Margins** tab: set exact margins; tick **Horizontally** and/or **Vertically** to centre on page.
4. **Sheet** tab: tick **Row and column headings** to print A, B, C… and 1, 2, 3…; tick **Gridlines** if required.

### 10.3 Printing Row and Column Headings on Every Page
1. **Page Layout** → **Print Titles**.
2. In **Rows to repeat at top**, click the selector and click the header row on the sheet.
3. Click **OK**.

### 10.4 Print Preview
- **File** → **Print** — shows a preview on the right.
- Use **Page Layout** view (**View** → **Page Layout**) to see margins and headers/footers visually.

### 10.5 Showing Formulas Instead of Values
1. Press **Ctrl + `** (backtick) to toggle formula display.
2. Print the spreadsheet showing formulas if the question asks for it.
3. Press **Ctrl + `** again to return to normal view.

---

## 11. Named Ranges

1. Select the cell range.
2. Click the **Name Box** (left of the Formula Bar, shows the cell address).
3. Type the name → press **Enter**.
4. Use the name in formulas instead of the cell reference (e.g. `=SUM(Sales)`).

---

## Common Mistakes to Avoid

| Mistake | How to Avoid |
|---|---|
| Relative reference when absolute needed | Use `$` signs; press F4 to toggle |
| VLOOKUP returns wrong value | Check col_index_num and use FALSE for exact match |
| Chart missing a title or axis label | Add via Chart Design → Add Chart Element |
| Data not sorted before filtering | Sort first if the question specifies a sort order |
| Formulas not copied to all required rows | Drag fill handle to the last data row |
| Wrong number format (e.g. integer instead of 2 d.p.) | Apply number format before printing |
| Print area not set correctly | Use Page Layout → Print Area → Set Print Area |
| Formulae visible in printed output | Toggle off Ctrl+` before printing unless asked |
