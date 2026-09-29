# SQL Learning Portfolio

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

This repository is a hands-on collection of SQL exercises, database projects, and
Python/SQLite integrations. It documents practical work with relational design,
queries, constraints, indexes, transactions, reporting, and database-backed
applications.

## Why this project is useful

- **Progressive practice:** Exercises cover table design, CRUD, joins, views,
  stored procedures, triggers, cursors, dynamic SQL, and permissions.
- **Runnable examples:** SQL scripts and SQLite database files provide data to
  inspect and query locally.
- **Realistic projects:** The CRM final project models customers, products,
  orders, and feedback, with CRUD operations and reporting queries.
- **Python integration:** A small interactive CLI demonstrates how Python's
  standard-library `sqlite3` module can manage a relational database.
- **Reference notes:** Markdown files record the goals, decisions, and results
  for each exercise.

## Getting started

### Prerequisites

- Git
- SQLite 3 for the SQLite examples
- Python 3 for the Python integrations
- A MySQL-compatible database client/server for the MySQL exercises in
  [`Practical_Exercises`](Practical_Exercises/)

There are no third-party Python dependencies. The Python examples use only the
standard library.

### Clone the repository

```bash
git clone https://github.com/VoidLance/SQL.git
cd SQL
```

### Run the CRM project

The final project includes an initialized SQLite database, its schema script,
and an interactive command-line application:

```bash
cd "Final Projects"
python3 main.py
```

Use the menu to create, list, update, and delete customers, products, orders,
and feedback, or to run customer-order, product-sales, and feedback-analytics
reports. Order values are calculated from product prices and tracked stock is
reduced when an order is created.

The implementation and schema are documented in
[`Final Projects/final_project.md`](Final%20Projects/final_project.md),
[`Final Projects/main.py`](Final%20Projects/main.py), and
[`Final Projects/final_project.sql`](Final%20Projects/final_project.sql).

### Run a SQL example directly

SQLite can execute any of the self-contained `.sql` scripts. For example:

```bash
sqlite3 /tmp/movies.db < "SQLite Data Analysis Practice/movies.sql"
```

Then open the database in SQLite or a database browser:

```bash
sqlite3 /tmp/movies.db
```

The corresponding walkthrough is in
[`SQLite Data Analysis Practice/practice.md`](SQLite%20Data%20Analysis%20Practice/practice.md).

## Repository guide

| Directory | Contents |
| --- | --- |
| [`Final Projects`](Final%20Projects/) | CRM database, Python CLI, ERD, and project notes |
| [`Practical_Exercises`](Practical_Exercises/) | Relational design, e-commerce, student information, advanced database, and F1 exercises |
| [`Python Integration`](Python%20Integration/) | A basic Python CRUD example using SQLite sales data |
| [`SQLite Data Analysis Practice`](SQLite%20Data%20Analysis%20Practice/) | Movie database schema and analysis queries |
| [`F1 Challenge`](F1%20Challenge/) | Formula 1 CSV data, SQLite database, and analysis SQL |

Most exercise directories contain an `exercises.md` or similarly named
walkthrough alongside the SQL script and sample data. The repository also
includes exported database files for exploring the completed exercises in a
database client.

## Documentation and support

- Start with the walkthrough in the directory for the database you want to
  study.
- Review the [CRM project notes](Final%20Projects/final_project.md) for the
  most complete end-to-end example.
- Search existing [GitHub issues](https://github.com/VoidLance/SQL/issues) or
  [open a new issue](https://github.com/VoidLance/SQL/issues/new) for questions,
  reproducible problems, or suggestions.

## Contributing

Contributions from learners and database practitioners are welcome. To propose
an improvement:

1. Fork the repository and create a focused branch.
2. Add or update the relevant SQL, data, or walkthrough.
3. Test SQL changes against the database engine they target and explain any
   setup assumptions.
4. Open a pull request describing the change and how it was checked.

Please keep examples focused, use parameterized SQL in application code, and
avoid committing credentials or private data. See [LICENSE](LICENSE) for the
project's license terms.

## Maintainer

Maintained by [Alistair Sweeting](https://github.com/VoidLance). Contributions
and constructive feedback are encouraged.
