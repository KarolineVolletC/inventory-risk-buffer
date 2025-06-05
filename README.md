# Inventory Risk Buffer Calculation ( average consumption + safety stock)

This project is a Python script that calculates the Ideal Safety Stock based on consumption data, current stock, and transfer price, using a statistical approach to estimate demand variability and lead time.

## Features

- Reads Excel files with consumption, current stock, and price data.
- Calculates average monthly consumption and estimated standard deviation.
- Automatically identifies the lead time (PDT) column.
- Calculates the Ideal Safety Stock using a 95% service level.
- Compares current safety stock with the ideal one.
- Generates an Excel file with results, formatting, and a comparison chart.
- Simple graphical interface for selecting input and output files.

## Requirements

- Python 3.x
- pandas
- openpyxl
- tkinter (included in most Python distributions)

## How to Use

1. Run the script `safety_stock_avg_plus_std.py`.
2. Select the Excel file with the input data.
3. Choose where to save the output Excel file.
4. Check the generated file containing calculation sheets and a comparison chart.

## Calculation Explanation

The Ideal Safety Stock calculation follows these steps:

- Average monthly consumption = Total consumption over 24 months / 24
- Estimated standard deviation = 20% of average monthly consumption
- Lead time converted from days to months
- Service level factor Z = 1.64 for 95%
- Safety Stock = Average consumption during lead time + Z × standard deviation × √(lead time in months)

---

## Author

Karoline Vollet Coelho

---

## License

MIT License

Copyright (c) 2025 [Karoline Vollet Coelho]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights 
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell 
copies of the Software, and to permit persons to whom the Software is 
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in 
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR 
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, 
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE 
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER 
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, 
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN 
THE SOFTWARE.
