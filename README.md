# mecaniQA-vitoria

Projeto de Modelos de Aprendizagem de Máquina — MecâniQA.

## Como rodar

1. Crie e ative o ambiente virtual:

```bash
python -m venv .venv
source .venv/bin/activate
```

2. Instale as dependências (incluindo pandas):

```bash
pip install -r requirements.txt
```

3. (Opcional) Registre o kernel do Jupyter:

```bash
python -m ipykernel install --user --name=mecaniqa --display-name="Python (mecaniQA)"
```

4. Abra o notebook e selecione o kernel **Python (mecaniQA)** ou o interpretador `.venv`.

5. Rode as células na ordem.

## Estrutura

- `data/mecaniqa_dataset.csv` — base de dados
- `01_inspecao_serie_temporal.ipynb` — Encontro 1 (importação e inspeção)
- `02_decomposicao_serie_temporal.ipynb` — Encontro 2 (decomposição T/S/R)
- `03_pipeline_previsao.ipynb` — Encontro 3 (Pipeline sklearn)
- `04_baseline_naive_media_movel.ipynb` — Encontro 4 (02/09/2026): Naive e média móvel sem data leakage
- `05_validacao_temporal_metricas.ipynb` — Encontro 5 (16/09/2026): Time Series Split, MAE, RMSE e MAPE
- `requirements.txt` — pacotes do projeto

## Boletim dos baselines (Time Series Split, 5 folds)

Métrica principal para o cliente (litros/dia em média): **MAE**.

| Baseline | MAE | RMSE | MAPE |
| --- | --- | --- | --- |
| Naive | 6,65 | 8,92 | 32,64% |
| Médias móveis (7 dias) | 7,36 | 8,09 | 37,22% |

**Vencedor: Naive.** Erra menos no dia a dia (MAE e MAPE). A média móvel tem RMSE menor: suaviza picos, mas erra mais em litros médios por dia.
