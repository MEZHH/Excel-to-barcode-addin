# Barcode List: Excel add-in

An Excel task pane that turns the first column of your sheet into a printable list of barcodes.

Based on the idea of [KyriakosGian/Barcode-List-From-Excel](https://github.com/KyriakosGian/Barcode-List-From-Excel) (Apache-2.0). Barcodes are drawn with [JsBarcode](https://github.com/lindell/JsBarcode).

## Features

- Reads column A of the active sheet, or the first column of your selection
- Barcode types: Code 128, Code 39, EAN-13, EAN-8, UPC-A, ITF-14
- Optional list name, barcode height, and number under each barcode
- Insert the barcodes into a new sheet as pictures, or print the preview
- Numbers that don't fit the chosen type are flagged instead of stopping the list

## Install

1. Download `manifest.xml` from this repository.
2. In Excel, load it as an add-in:
   - **Excel on the web:** Insert > Add-ins > Manage My Add-ins > Upload My Add-in
   - **Excel on Windows:** add a shared folder containing the manifest under File > Options > Trust Center > Trusted Add-in Catalogs, then Insert > My Add-ins > Shared Folder
   - **Excel on Mac:** copy the manifest to `~/Library/Containers/com.microsoft.Excel/Data/Documents/wef`, restart Excel, then Insert > My Add-ins
3. Click **Barcode List** on the Home tab.

The add-in page is hosted at https://mezhh.github.io/Excel-to-barcode-addin/ and needs an internet connection.

## Tips

- Format the column as Text before typing codes that start with 0, or Excel will drop the leading zeros.
- Code 128 accepts any text. EAN-13 needs 12 or 13 digits, EAN-8 needs 7 or 8, and UPC-A needs 11 or 12.
- Requires Excel API 1.9 (Microsoft 365, Excel 2021 or later, and Excel on the web).
