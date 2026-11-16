# Dados

## Dataset de entrada (não incluído no repositório)

[Kepler & TESS Exoplanet Data](https://www.kaggle.com/datasets/vijayveersingh/kepler-and-tess-exoplanet-data), no Kaggle: sete tabelas do NASA Exoplanet Archive (versão de 03/02/2025). Não redistribuo os arquivos aqui; baixe direto da fonte:

```bash
pip install kaggle        # precisa de ~/.kaggle/kaggle.json (Kaggle > Settings > Create New Token)
kaggle datasets download -d vijayveersingh/kepler-and-tess-exoplanet-data --unzip -p data/raw
```

Ou baixe pelo site e extraia em `data/raw/`. O notebook procura os arquivos pelo nome (aceita datas com pontos ou com underscores).

## Arquivo incluído

- `features_lc_1000.csv`: features extraídas das curvas de luz do Kepler para 1.000 KOIs (500 `CONFIRMED` + 500 `FALSE POSITIVE`), geradas pela seção 5.1 do notebook (≈82 min). Colunas: `snr_emp`, `odd_even_sigma`, `sec_sigma`, `core_ratio`, `depth_vs_cat` e auxiliares. Permite rodar a análise sem baixar as curvas do MAST.
