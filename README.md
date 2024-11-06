# NFT Metadata Scraper

## Overview

The **NFT Metadata Scraper** is a Python tool designed to collect metadata information for NFTs from an API endpoint or IPFS link. It retrieves key details such as name, description, image, and attributes for each NFT and saves the data in a structured CSV format for further analysis.

### Features

- **Fetch Metadata**: Retrieves metadata for NFTs based on a provided list of token IDs.
- **Attribute Extraction**: Extracts custom attributes, flattening them into a structured format.
- **CSV Output**: Saves the results to a CSV file for easy viewing, filtering, and analysis.

### Prerequisites

To use this script, you’ll need:

1. Python 3.x
2. Required libraries: `requests` and `pandas`

Install the required libraries with:

```bash
pip install requests pandas
```

### Usage

#### Step 1: Update the Base URL and Token IDs

Update the `base_url` in the script to point to the API endpoint for the specific NFT platform or IPFS location where metadata is hosted. For example, for OpenSea, you may use an endpoint such as:

```python
base_url = "https://api.opensea.io/api/v1/asset/YOUR_CONTRACT_ADDRESS"
```

Also, populate `token_ids` with the IDs of the NFTs whose metadata you wish to scrape.

#### Step 2: Run the Script

Run the script using the following command:

```bash
py nft_metadata_scraper.py
```

The script will fetch metadata for each NFT specified in `token_ids`, extract relevant information, and save it to a CSV file.

### Example

If the base URL is set to an example platform and token IDs are `[1, 2, 3]`, the command to run would look like:

```bash
py nft_metadata_scraper.py
```

The script outputs a CSV file named `nft_metadata.csv` with columns for each metadata field.

### Data Output

The CSV file will include columns such as:

- **Name**: NFT name
- **Description**: Description of the NFT
- **Image**: URL to the NFT image
- **Attributes**: Each attribute (e.g., "Background", "Rarity") appears in its own column with respective values

### Important Notes

- **Rate Limiting**: Some NFT platforms may have rate limits. You may need to add a delay between requests to avoid being blocked.
- **Variable Metadata**: Different NFT collections may have different metadata structures. You may need to adjust the `extract_metadata` method to fit your collection’s metadata fields.

### Limitations

- **IPFS Gateway Access**: If metadata is stored on IPFS, ensure you’re using an accessible IPFS gateway (e.g., https://ipfs.io/ipfs/).
- **Platform Compatibility**: Modify the base URL, token IDs, and possibly `extract_metadata` if working with a platform that has a different metadata structure.

### Future Enhancements

- **Automated Platform Detection**: Detect metadata formats for specific platforms automatically.
- **Extended Storage Options**: Add support for storing metadata in a database for better search and analysis capabilities.
- **Metadata Validation**: Add checks to ensure all required metadata fields are present.

--- 

This script provides a framework for NFT metadata scraping but may require adjustments based on the specific NFT platform you’re working with. Let me know if you need help with any particular platform setup or have questions about handling custom metadata fields.print('vpadcfbmbs')