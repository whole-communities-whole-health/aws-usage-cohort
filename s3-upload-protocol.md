## S3 Upload Protocol for lab data

This is an example of a simple data structure and data dictionary that worked for a WCWH lab. It is a table in a spreadsheet that becomes a database table when uploaded. The lab used a single table with participant ID as the first column, and multiple additional columns to accommodate measured variables.
 
| participant_id | sample_date | string_metric | integer_metric | column_name_E |
|----------------|-------------|---------------|----------------|---------------|
| P0001T         | 5/1/23      | test-string   | 42             | null          |
| P0002T         | 5/2/23      | test-string   | 42             | null          |
| P0004T         | 5/2/23      | test-string   | 42             | null          |
| P0006T         | 5/2/23      | test-string   | 42             | null          |
| P0007T         | 5/1/23      | test-string   | 42             | null          |
| P0008T         | 5/2/23      | test-string   | 41             | null          |
| P0009T         | 5/3/23      | test-string   | 42             | null          |
| P0011T         | 5/3/23      | test-string   | 42             | null          |
| P0014T         | 5/1/23      | test-string   | 42             | null          |
| P0015T         | 5/3/23      | test-string   | 42             | null          |


## Data dictionary for table

The table above requires a data dictionary to define what the table itself is for, the meaning of each column heading:

| Table Name        | Table Definition                 | Field          | Field Definition                        |
|-------------------|----------------------------------|----------------|-----------------------------------------|
| sample table name | explanation of your table's data | participant_id | participant identifier                  |
| --                | --                               | sample_date    | date of sample collection               |
| --                | --                               | string_metric  | explanation of the text in this field   |
| --                | --                               | integer_metric | answer to the ultimate question of life |
| --                | --                               | column_name_E  | some other description for column E     |

## Follow the guidelines below for a successful upload to the database:

- All uploaded data should be deidentified

- Your first column should be participant ID. This is a unique identifier for each participant.

- Use the csv file format

- Use an underscore instead of a space in column headings. For example, “column_name” instead of “column name”

- Column names should be descriptive and include units wherever possible

- If gender is included as a variable and is numerically coded, then use 0 for female and 1 for male to maintain consistency with other database values.

- Create a data dictionary explaining the meaning of each column so that other researchers understand the data.

- Include only minimal demographic info. Adult and child demographic information is available in a separate database table. 

- Formatting (highlights, bold or italicized fonts, conditional formatting) won't be visible to others in the database.

- Do not use merged cells. The top row (row 1) should have only the column headings of each column and no additional information. Participant ID should be the first column, and any number of additional columns to accommodate other variables.

- Use “null” or a similar placeholder for missing values in spreadsheet rather than leaving a value blank. When downloaded from the database later, blank cells in a spreadsheet can be interpreted to be zero by some software. 

- Standardize values of none/NA/missing to a single value. Use NULL for all missing values if you don’t already have a preference. It may make sense for your group to use a combination of null and a separate identifier to make a distinction between data that is missing vs data not currently available.

- Rename duplicate column headings in your spreadsheet (e.g. visit_one and visit_two). It may be appropriate for your group to have multiple tables (e.g. visit_one_table and vistit_two_table) rather than many near duplicate column headings in a single table.

- Use UTC for timestamps. Use the format YYYY-MM-DD HH:mm:ss (and fractional seconds, if desired. An example is 2024-02-16 23:51:04.728014.

\
[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fwhole-communities-whole-health%2Faws-usage-cohort%2Fblob%2Fmain%2Fs3-upload-protocol.md&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)
