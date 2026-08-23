# Modelet e Trajnuara

Peshat e modeleve fine-tuned (DistilBERT ~540MB, XLM-RoBERTa ~1.1GB) **nuk përfshihen** në këtë repository për shkak të madhësisë. Ato janë të disponueshme si output i notebooks përkatëse në Kaggle:

| Model | Notebook (Kaggle) | Madhësia |
|---|---|---|
| DistilBERT (fine-tuned) | `distilbert-finetuning` — tab "Output" → `distilbert-final-model/` | ~540 MB |
| XLM-RoBERTa (fine-tuned) | Rikuperuar si dataset i ri `xlmr-finetuned-model` (nga backup lokal), përdorur te `xlmr-error-analysis` | ~1.1 GB |

## Si të riprodhosh modelet

Ekzekuto notebooks te `notebooks/kaggle/` sipas rradhës:

1. `distilbert-finetuning.ipynb` → prodhon `distilbert-final-model/`
2. `xlm-roberta-finetuning.ipynb` → prodhon `xlmr-final-model/`
3. `distilbert-error-analysis.ipynb` → inference + error analysis mbi DistilBERT (kërkon output nga hapi 1 si input)
4. `xlmr-error-analysis.ipynb` → inference + error analysis mbi XLM-R (kërkon modelin nga hapi 2 si input)

**Kërkohet**: GPU (Kaggle T4 ose ekuivalent), ~1-2.5 orë për model.
