# Modelet e Trajnuara

Peshat e modeleve fine-tuned (DistilBERT ~540MB, XLM-RoBERTa ~1.1GB) **nuk perfshihen** ne kete repository per shkak te madhesise. Ato jane te disponueshme si output i notebooks perkatese ne Kaggle:

| Model | Notebook (Kaggle) | Madhesia |
|---|---|---|
| DistilBERT (fine-tuned) | `distilbert-finetuning` — tab "Output" → `distilbert-final-model/` | ~540 MB |
| XLM-RoBERTa (fine-tuned) | Rikuperuar si dataset i ri `xlmr-finetuned-model` (nga backup lokal), perdorur te `xlmr-error-analysis` | ~1.1 GB |

## Si te riprodhosh modelet

Ekzekuto notebooks te `notebooks/kaggle/` sipas rradhes:

1. `distilbert-finetuning.ipynb` → prodhon `distilbert-final-model/`
2. `xlm-roberta-finetuning.ipynb` → prodhon `xlmr-final-model/`
3. `distilbert-error-analysis.ipynb` → inference + error analysis mbi DistilBERT (kerkon output nga hapi 1 si input)
4. `xlmr-error-analysis.ipynb` → inference + error analysis mbi XLM-R (kerkon modelin nga hapi 2 si input)

**Kerkohet**: GPU (Kaggle T4 ose ekuivalent), ~1-2.5 ore per model.
