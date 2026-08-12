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

4. Abra o notebook `01_inspecao_serie_temporal.ipynb` e selecione o kernel **Python (mecaniQA)** ou o interpretador `.venv`.

5. Rode as células na ordem.

## Estrutura

- `data/mecaniqa_dataset.csv` — base de dados
- `01_inspecao_serie_temporal.ipynb` — Encontro 1 (importação e inspeção)
- `requirements.txt` — pacotes do projeto
