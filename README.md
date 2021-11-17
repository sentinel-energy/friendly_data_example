# Example data package for Friendly data tools

**NOTE**: The datasets included in this package are based on a real
Calliope model, however it has been heavily simplified to illustrate
the use case of the Friendly data tools, and should not be considered
accurate

## Files

- `conf.yaml`: configuration for metadata and IAMC conversion
- `index.yaml`: configuration identifying different index columns,
  important for dataset metadata
- `technology.csv`: technology definitions for IAMC conversion
- `carrier.csv`: carrier definitions for IAMC conversion
- `*.csv`: datasets (besides the two above)
- `datapackage.json`: data package metadata

## Example commands

- Create the package (writes the `datapackage.json` file)

      $ friendly_data create index.yaml --metadata=conf.yaml --inplace

- Describe the data package

      $ friendly_data describe .

- Convert to IAMC (written to `iamc.csv`)

      $ friendly_data to-iamc conf.yaml index.yaml iamc.csv
