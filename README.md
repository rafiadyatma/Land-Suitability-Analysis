# Land-Suitability-Analysis
This project performs a GIS-based Land Suitability Analysis to identify suitable locations for new residential development. Using elevation, road, river, and land-use data, each criterion is scored (0–10), weighted, and combined through raster analysis in ArcGIS to produce a final suitability map.


# Land Suitability Analysis (GIS)

This project performs a GIS-based land suitability analysis using a scoring and weighting approach. The analysis evaluates multiple spatial criteria to identify suitable areas based on accessibility, terrain conditions, land cover, and environmental constraints.

---

## 1. Scoring and Weighting Tables

### 1.1 Distance to Road Score

| Distance (m) | Score |
|--------------|-------|
| 0 – 200      | 10    |
| 200 – 400    | 9     |
| 400 – 600    | 8     |
| 600 – 800    | 7     |
| 800 – 1000   | 6     |
| > 1000       | 5     |

---

### 1.2 Slope Score

| Slope (%) | Score |
|-----------|-------|
| ≥ 3       | 10    |
| 3 – 6     | 9     |
| 6 – 9     | 7     |
| 9 – 12    | 5     |
| > 12      | 1     |

---

### 1.3 Criteria Weighting

| Criteria | Weight |
|--------|--------|
| Slope  | 20%    |
| Road   | 50%    |
| Land Use | 30%  |

---

### 1.4 Land Use / Land Cover Score

| Land Use Type | Score |
|--------------|-------|
| Hutan Lahan Kering Primer | 7 |
| Tanah Terbuka | 10 |
| Hutan Lahan Kering Sekunder | 7 |
| Pertanian Lahan Kering | 6 |
| Hutan Tanaman Industri (HTI) | 5 |
| Semak / Belukar | 8 |
| Perkebunan | 6 |
| Tubuh Air | 0 |
| Hutan Mangrove | 6 |
| Sawah | 6 |
| Rawa | 0 |
| Pemukiman | 7 |

---

### 1.5 River Buffer Constraint

| Distance (m) | Status |
|--------------|--------|
| 0 – 200      | Not Allowed |
| > 200        | Allowed |

---

## 2. Criteria Score Map Layouts

The following maps are generated to visualize suitability scores for each criterion:

- **Distance to Road Score Map**
![image_alt](https://github.com/rafiadyatma/Land-Suitability-Analysis/blob/f4840597d29a15ff56e63fd93fdc222a933663d3/layout_Views/skor_jarak_ke_jalan.png)

- **Slope Score Map**
![image_alt](https://github.com/rafiadyatma/Land-Suitability-Analysis/blob/f4840597d29a15ff56e63fd93fdc222a933663d3/layout_Views/skor_kemiringan_lahan.png)

- **Land Use Score Map**
![image_alt](https://github.com/rafiadyatma/Land-Suitability-Analysis/blob/f4840597d29a15ff56e63fd93fdc222a933663d3/layout_Views/skor_tutupan_lahan.png)

- **River Buffer Map**
![image_alt](https://github.com/rafiadyatma/Land-Suitability-Analysis/blob/f4840597d29a15ff56e63fd93fdc222a933663d3/layout_Views/buffer_sungai_200.png)

---

## 3. Final Suitability Score Map
![image_alt](https://github.com/rafiadyatma/Land-Suitability-Analysis/blob/f4840597d29a15ff56e63fd93fdc222a933663d3/layout_Views/skor_akhir_layout.png)

The final land suitability map is produced by combining all scored criteria using a weighted overlay approach. Areas within restricted river buffer zones are excluded from the final result.

This output map represents the overall land suitability based on all defined criteria.
