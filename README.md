This project implements an automated pipeline for extracting data from side-by-side tables within images.

Preprocessing: Utilizes OpenCV for grayscale conversion and binary thresholding to isolate table structures.

Contour Detection: Employs a vertical rectangular kernel to identify distinct table blocks and bounding boxes.

Spatial Sorting: Sorts detected regions by X-coordinates to ensure data is processed in a consistent left-to-right order.

OCR & Data Structuring: Leverages PyTesseract (PSM 6) for character recognition and cleans the output into structured Pandas DataFrames.

Horizontal Merging: Automatically concatenates multiple table results into a single, unified side-by-side dataset.

 rows = [line.strip().split() for line in data.strip().split('\n') if line.strip()] - this part needs further optimization for efficiently handeling the split
