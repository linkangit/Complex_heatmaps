# Complex Heatmap Example in Python

A demonstration of how to create a more advanced “complex heatmap” with multiple row and column annotations, custom clustering, and a combined legend.

---

## Overview

In this repository, we showcase a script that does the following:

1. Generates random gene-expression-like data (rows = samples, columns = genes).  
2. Introduces multiple annotations on the rows (e.g., “Condition” and “Batch”) and columns (e.g., “Gene Family” and “Chromosome”).  
3. Clusters rows and columns using a customizable linkage method and distance metric.  
4. Normalizes or standardizes the data (optional).  
5. Produces a combined legend that shows all annotation color mappings.

---

## Key Features

- **Multiple Row Annotations:** Each sample (row) has a “Condition” (Control, TreatmentA, TreatmentB) and a “Batch” (Batch1, Batch2).  
- **Multiple Column Annotations:** Each gene (column) belongs to a “Gene_Family” (Kinase, Transcription_Factor, Transporter) and a “Chromosome” (Chr1, Chr2, Chr3).  
- **Custom Clustering:** The script specifies a linkage method (for instance, ‘ward’) and distance metric (for instance, ‘euclidean’).  
- **Standardization:** Rows can be standardized to have zero mean and unit variance, making cross-sample comparisons more direct.  
- **Comprehensive Legend:** A separate, combined legend clarifies row and column annotation colors in one place.

---

## Requirements

- Python 3.x  
- NumPy  
- pandas  
- matplotlib  
- seaborn  

Install via:pip install numpy pandas matplotlib seaborn

## Data Generation

- A simple matrix of random numbers simulates gene expression.  
- Each of the 12 samples (rows) is labeled as “Sample_1” through “Sample_12.”  
- Each of the 8 genes (columns) is labeled as “Gene_1” through “Gene_8.”  

---

## Annotations

1. **Row Annotations**  
   - Condition → Mapped to colors (e.g., Control → green).  
   - Batch → Mapped to colors (e.g., Batch1 → purple).

2. **Column Annotations**  
   - Gene_Family → Mapped to colors (e.g., Kinase → brown).  
   - Chromosome → Mapped to colors (e.g., Chr1 → yellow).

Each category is assigned a unique color and translated into color arrays for Seaborn’s clustermap.

---

## Clustermap

- **Clustering**: Rows and columns can both be clustered using a specified linkage (`'ward'`, `'complete'`, etc.) and distance metric (`'euclidean'`, `'manhattan'`, etc.).  
- **Standardization**: By specifying `z_score=0` or `standard_scale=1`, you can adjust rows or columns to facilitate comparison.  
- **Figure Size**: Adjusted dimensions help readability when dealing with many samples or genes.  
- **Annotation Bars**: Row and column annotation bars automatically display next to the heatmap, colored according to the mapping dictionaries.

---

## Legend

- The script manually generates legend patches that match each annotation color.  
- These patches are combined and placed in a single legend, offset to the right of the figure.

---

## Usage

1. Download or clone the repository.  
2. Open and run the script (named something like “complex_heatmap.py”).  
3. A figure window displaying the complex heatmap will appear.  

You can modify sample size, gene count, or annotation categories in the script to match your needs.

---

## Contributing

Contributions are welcome! Feel free to fork the repository, make changes, and submit a pull request. You can also open an issue for bug fixes or feature requests.

---

## License

This project is released under the [MIT License](LICENSE), so you’re free to modify and reuse it as needed.

