# Genshin Impact Character Data

This repository contains structured data for characters from Genshin Impact. The information is extracted and cleaned from the Genshin Impact Wiki (Fandom). All the information is upto date. Purpose of this is just easy understanding and usage.

**Current Version**: Luna VI

## Files

- **`characters.json`**: The primary data source. It includes full metadata, is lowercased for consistency, and is sorted chronologically by game version.
- **`characters.csv`**: A flattened version of the dataset. It removes array types, uses standard naming conventions (spaces instead of dashes), and is sorted alphabetically by character name.

## Data Schema

Each character entry contains the following fields:

| Field | Description | Type |
| :--- | :--- | :--- |
| `id` | Unique identifier using lowercase slugs (e.g., `kaedehara-kazuha`). | String |
| `name` | The character's full name with spaces (CSV only). | String |
| `names` | An array containing names that people usually use for that character (JSON only). | Array |
| `rarity` | Character star rating (e.g., `4 stars`). | String |
| `element` | The character's Vision/Element. | String |
| `weapon` | The type of weapon used. | String |
| `region` | The character's associated nation or region. | String |
| `release_date` | The official release date of the character. | String |
| `version` | The game version in which the character was introduced. | String |
| `image_url` | Direct link to the high-resolution character icon asset. | String |
| `wiki_url` | Direct link to the character's Fandom Wiki page. | String |

## Data Formatting

To ensure the data is programmatically friendly, the following conventions were applied:

1. **Lowercase**: All text data (except for case-sensitive URLs) has been converted to lowercase.
2. **High-Resolution Assets**: Image URLs have been stripped of thumbnail parameters to point directly to the original high-resolution files.
3. **Sorting**:
   - The **JSON** file follows a pattern-based sort according to game versions (`1.x`, `2.x`, etc.).
   - The **CSV** file is sorted alphabetically by the `name` column.
4. **Clean IDs**: Underscores from the original Wiki source have been replaced with dashes for the `id` and spaces for the `name`.

## Disclaimer

This dataset is intended for educational and fan-project purposes. All character data and assets are the property of HoYoverse. This repository is not affiliated with or endorsed by HoYoverse or the Genshin Impact Wiki.
