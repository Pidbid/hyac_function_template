# hyac_function_template
Function template for hyac

## Function Template Structure

This project uses a JSON-based format for defining serverless functions. Each `.json` file represents a single function and its dependencies.

### JSON Schema

- `name` (string): The name of the function.
- `create_at` (string): The creation timestamp (e.g., "YYYY-MM-DD HH:MM:SS").
- `update_at` (string): The last update timestamp (e.g., "YYYY-MM-DD HH:MM:SS").
- `dependencies` (object): Describes the external Python dependencies.
  - `name` (string): The name of the dependency package (e.g., from pip).
  - `version` (string): The required version of the dependency.
- `code` (string): The Python source code of the function, formatted as a single string with escaped newlines (`\n`).

### Example

```json
{
    "name": "example_function",
    "create_at": "2025-01-01 00:00:00",
    "update_at": "2025-01-01 00:00:00",
    "dependencies": {
        "name": "some-library",
        "version": "1.2.3"
    },
    "code": "def handler(context, ...):\\n    # Your function logic here"
}
```
