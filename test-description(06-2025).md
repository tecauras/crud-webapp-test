# E-commerce Web App (CRUD)Test Requirements for Intern Hiring

**Objective**: Build a web app to manage categories and products with Excel file upload, database operations, and basic CRUD functionality. 

> **Deadline**: Complete as much functionality as possible within 3 days from the date of receipt.
> 

**Database Schema**:

1. **Category Table**:
    - `category_id` (PK, Auto-increment, Integer)
    - `category_name` (Varchar, Not Null, Unique)
    - `description` (Text, Nullable)
2. **Products Table**:
    - `product_id` (PK, Auto-increment, Integer)
    - `product_name` (Varchar, Not Null)
    - `category_id` (FK to Category, Integer)
    - `price` (Decimal, Not Null)
    - `stock` (Integer, Not Null)

**Excel File Format**:

- Two sheets:
    1. **Products**:
        - Columns: `product_name`, `category_name`, `price`, `stock`

**Functional Requirements**:

1. **Category Management**:
    - Form to create a category (`category_name`, `description`).
    - Validate: `category_name` not empty, unique.
    - Display categories in a table.
2. **Excel Upload**:
    - Upload excel file.
    - Read **Products** sheet, insert into Products table:
        - Map `category_name` to `category_id`.
        - Validate: `price` > 0, `stock` >= 0, `category_name` exists.
    - Show success/failure message with error details.
3. **Data Display**:
    - Two tables:
        - **Categories**: `category_id`, `category_name`, `description`.
        - **Products**: `product_id`, `product_name`, `category_name` (via join), `price`, `stock`.
4. **Edit Functionality**:
    - **Products**: Edit button per row, form to update `product_name`, `category_id`, `price`, `stock`. Validate inputs.

**Technical Requirements**:

- **Backend**: Any language/framework (e.g.,NextJs, Node.js, Python(FastAPI/FlaskDjango)  ).
- **Database**: Relational (e.g., MySQL, PostgreSQL, SQLite).
- **Frontend**: HTML, CSS, JavaScript (Preferably: React, Vue, Next.js, Nuxt.js,Angular).
- **Validation**: Validate all inputs (form, Excel). Show clear error messages.
- **Security**: Validate file type, handle uploads securely.

**Deliverables**:

- Implement as much functionality as possible within a 3-day timeframe.
- Source code (backend, frontend).
- SQL file for schema and sample data.
- Sample Excel file.
- README: Setup instructions, run guide, Excel format explanation.

**Notes**:

- Ensure categories exist before Excel upload.to Excel.uploadingo Excel.
- Keep the UI simple and focus on functionality.
- Please refer to the other html files in the repo for design reference