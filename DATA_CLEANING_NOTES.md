# Data Cleaning Notes

## Comparison Rule
The latest 2026 registration date is **4 September 2026**. Therefore, the analysis compares **1 January–4 September 2026** with **1 January–4 September 2025**.

## Cleaning Steps Performed

### 1. Duplicate Registrations
Duplicate registration IDs were identified and removed. The first valid occurrence was retained.

### 2. Test / Invalid Records
Obvious test records, including TEST IDs and records containing test student/school labels, were removed.

### 3. Competition Names
Abbreviated competition names such as `Intl. Coding Olympiad` were standardized to their full versions such as `International Coding Olympiad`.

### 4. School Names
Uppercase and abbreviated variants of the same school were standardized to one consistent name.

### 5. Missing Values
Blank school, city, and registration-source values were retained as valid registrations and labelled `Unknown` rather than deleting the entire row.

### 6. Date Formats
Mixed date formats were converted into consistent Excel date values so monthly and weekly trend analysis could be performed correctly.

### 7. City / Country Consistency
For known cities with obvious country mismatches, country values were standardized using a city-country mapping. The original country value was retained in a separate field for transparency.

### 8. Public GitHub Privacy
Student names and registration IDs in the GitHub version have been replaced with anonymous labels. The original source files contain personal data and are intentionally excluded from the public repository.
