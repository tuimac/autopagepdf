# Create web page PDF automatically
[![CircleCI](https://circleci.com/gh/tuimac/autopagepdf.svg?style=shield)](https://circleci.com/gh/tuimac/autopagepdf)

This tool is the web page PDF printing automation tool. If you define the web page urls, PDF file name in Excel, this tool execute to take PDF for the target web pages.

## How to use
### 1.Define the target urls on Excel
Like below picture, you need to define PDF file name and the target urls you want to make PDF.<br/>
<img width="387" alt="Screenshot 2022-12-31 at 9 00 41" src="https://user-images.githubusercontent.com/18078024/210119296-411c1d5c-42f5-4a9e-8e4a-e2fa4fe24c4d.png">

### 2.Download the AutoPagePDF packages.
You need to download the packages from [this link here](http://autopagepdf.tuimac.com/).<br/>
<img width="408" alt="Screenshot 2022-12-31 at 10 48 42" src="https://user-images.githubusercontent.com/18078024/210121486-929858dc-700d-46f6-b3d4-57e05c1efa67.png">

### 3.Change the parameters in config.json
There is config.json file in the package you download before.<br/>
The meaning of each parameter is below:

| Key| Value |
| ----- | ----- |
| EXCEL_FILE_PATH | Excel file path you define the url and file name. |
| EXCEL_SHEET_NAME | The sheet name in the Excel workbook you define the url and file name. |
| EXCEL_DATA_CONFIG | **●START_ROW**: This script read each row value in Excel sheet so define where you want to start.<br/>**●ID_COLUMN**</font>: PDF file name colume number. Excel column number start from 1. Ex) A column is 1.<br/>**●URL_COLUMN**: Url column number. Excel column number start from 1. Ex) A column is 1. |
| LOG_FILE_PATH | Log file path for debug this program. You need to choose the folder or directory you have the grant to create the file. |
| ERROR_URL_LIST_FILE | The list file which collect the invalid urls. You need to choose the folder or directory you have the grant to create the file. |
| INTERVAL | The interval for reading each row in the defined Excel worksheet. Unit is seconds. |
| EXCLUDE_WORDS | These are the grep words for the valid url page which you want to skip the page included these words. |

### 4.Execute AutoPagePdf
Just execute AutoPagePdf binary in the package.

## Authors

* **tuimac** - [tuimac](https://github.com/tuimac)

If you have some opinions and find bugs, please post [here](https://github.com/tuimac/autopagepdf/issues).

## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
