# Information Events Data Source

This data source provides an integration for retrieving and filtering "Information Events" from a DataMiner System (DMS).

## Features

- **Time-based filtering:**  
  Information events from a specific start date/time (`From`) and, optionally, up to an end date/time (`Until`).

- **Searching:**  
  Sezrch information events, matching against both the type and value.

- **Efficient Paging:**  
  Handles large result sets with server-side paging.

- **Columns:**  
  Returns the following columns for each event:
  - `Origin` (Element Name)
  - `Type` (Parameter Description)
  - `Value`
  - `Time` (UTC)
  - `ID` (Alarm/Event ID)

## Input Arguments

| Argument      | Type      | Required | Description                                 |
|---------------|-----------|----------|---------------------------------------------|
| From          | DateTime  | Yes      | Start of the time range to query            |
| Until         | DateTime  | No       | End of the time range to query              |
| Search term   | String    | No       | Text to search in parameter name or value   |

## Usage

1. **Configure the Data Source:**  
   Add the data source to your GQI dashboard or app, referencing it as "Information Events".

2. **Set Input Arguments:**  
   - Specify the `From` date/time to define the start of your query window.
   - Optionally, set the `Until` date/time to limit the range.
   - Optionally, provide a `Search term` to filter results.

3. **Query Results:**  
   The data source will return a paged list of information events matching your criteria, with the columns described above.

## Sample Dashboard

A sample dashboard called `Information Events` is automatically added to your system.

![Sample dashboard](./SLC-GQIDS-InformationEvents/CatalogInformation/Images/dashboard.png)

## Important
Support for this data source using the GQI DxM is currently under development.
