# Të dhënat

Për shkak të madhësisë (dataset-i origjinal ~8.6 GB, dataset-i final i përpunuar ~50-100 MB), file-t CSV **nuk përfshihen** në këtë repository. Ndiqni hapat e mëposhtëm për t'i riprodhuar.

## 1. Shkarko dataset-in origjinal

```powershell
kaggle datasets download -d gentrexha/kosovo-news-articles-dataset -p data/raw --unzip
```

(Kërkon Kaggle API të konfiguruar — dokumentacionin zyrtar(https://github.com/Kaggle/kaggle-api))

## 2. Ndërto dataset-in final

Ekzekuto notebooks te `notebooks/local/` me këtë rradhë:

1. `explore.ipynb` — EDA, identifikimi i problemeve strukturore (taksonomi jokonsistente, multi-portal bias)
2. `ndertimi_dataset.ipynb` — ndërtimi i mapping-ut universal të kategorive dhe dataset-it të balancuar (`data/processed/dataset_final.csv`)
3. `preprocessing.ipynb` — pastrimi i tekstit dhe train/val/test split (`data/processed/train.csv`, `val.csv`, `test.csv`)

## Struktura pritur pas riprodhimit

```
data/
├── raw/
│   └── Kosovo-News-Articles.csv       (~8.6 GB, nga Kaggle)
└── processed/
    ├── dataset_final.csv               (~108,000 rreshta, i balancuar)
    ├── dataset_clean.csv                (pas pastrimit të tekstit)
    ├── train.csv                        (70%)
    ├── val.csv                          (15%)
    └── test.csv                         (15%)
```

## Taksonomia e kategorive

9 kategori finale, të ndërtuara përmes mapping-ut të variantave/sinonimeve nëpër portale të ndryshme:

**Botë, Ekonomi, Kulturë, Kuriozitete, Lifestyle, Politikë, Showbiz, Shëndet, Sport**

Shih `notebooks/local/ndertimi_dataset.ipynb` për hartën e plotë të mapping-ut (`KATEGORI_MAPPING`).
