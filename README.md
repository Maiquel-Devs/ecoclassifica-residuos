# ecoclassifica-residuos

Classificador de resíduos recicláveis (metal, plástico e papelão) com um modelo do Teachable Machine treinado no dataset TrashNet, usado no trabalho de Fundamentos de IA (Univille) para medir a acurácia nas imagens de teste.

## Requisitos

- Python 3.12
- Git

## Passo a passo

1. Clone o repositório e entre na pasta:

   ```
   git clone https://github.com/Maiquel-Devs/ecoclassifica-residuos.git
   cd ecoclassifica-residuos
   ```

2. Crie o ambiente virtual:

   ```
   python -m venv .venv
   ```

3. Ative o ambiente no Windows:

   ```
   .venv\Scripts\activate
   ```

   No PowerShell, se o bloqueio de scripts impedir a ativação, rode antes
   `Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass`.

4. Instale as dependências:

   ```
   pip install -r requirements.txt
   ```

5. Registre o ambiente como kernel do Jupyter:

   ```
   python -m ipykernel install --user --name ecoclassifica-residuos --display-name "Python (ecoclassifica)"
   ```

6. Abra o `analise_acuracia.ipynb` (no PyCharm, no VS Code ou com `jupyter notebook`), escolha o kernel **Python (ecoclassifica)** e rode todas as células de cima para baixo. O notebook calcula a acurácia por classe e geral, lista os erros e salva `resultados_teste.csv` na raiz do projeto.

## Estrutura das pastas

```
ecoclassifica-residuos/
├── analise_acuracia.ipynb      # notebook de análise de acurácia
├── requirements.txt            # dependências com versões fixas
├── README.md
└── TrashNet/
    ├── Dataset/
    │   ├── ImagemTreino/       # cardboard_100, metal_100, plastic_100
    │   └── ImagemTeste/        # cardboard_20, metal_20, plastic_20
    └── Modelo/                 # keras_model.h5, labels.txt, model.json,
                                # weights.bin, metadata.json
```

## Créditos

O dataset TrashNet foi criado por Gary Thung e Mindy Yang e está sob licença MIT.
Fonte utilizada: https://www.kaggle.com/datasets/feyzazkefe/trashnet
