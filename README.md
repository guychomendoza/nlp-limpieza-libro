# Normalización y Lematización de un libro

Checkpoint 3 de Procesamiento de Lenguaje Natural (Hybridge).

Pipeline de limpieza de texto en español aplicado a un libro completo: carga con reparación de codificación, limpieza con regex, tokenización, eliminación de stopwords, lematización con spaCy y comparativa contra stemming de NLTK.

## Estructura

```
├── limpieza_libro.ipynb   # Desarrollo de la limpieza
├── libro.txt              # Libro a procesar
├── requirements.txt       # Dependencias congeladas
└── salida/                # Se genera al ejecutar el notebook
    ├── corpus_lematizado.txt
    └── frecuencias.csv
```

## Cómo ejecutarlo

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS / Linux
source .venv/bin/activate

pip install -r requirements.txt
```

Abre `limpieza_libro.ipynb` en VS Code o Jupyter, selecciona el kernel de `.venv` y ejecuta todas las celdas.

## Libro

`libro.txt` — *[El sombrero de tres picos]*, de *[Pedro Antonio de Alarcón]*. Fuente: [Project Gutenberg](https://www.gutenberg.org/).
