# Normalización, lematización y vectorización de un libro

Checkpoints 3 y 4 de Procesamiento de Lenguaje Natural (Hybridge).

- **Checkpoint 3: limpieza.** Pipeline de texto en español aplicado a un libro completo: carga con reparación de codificación, limpieza con regex, tokenización, eliminación de stopwords, lematización con spaCy y comparativa contra stemming de NLTK.
- **Checkpoint 4: representación vectorial.** Bag-of-Words (`CountVectorizer`) y TF-IDF (`TfidfVectorizer`) sobre las oraciones del libro, TF-IDF y similitud coseno entre capítulos, y reducción a 3D con PCA para comparar ambos espacios.

## Estructura

```
├── limpieza_libro.ipynb   # Limpieza (secciones 1-8) y vectorización (9-13)
├── libro.txt              # Libro a procesar
├── requirements.txt       # Dependencias congeladas
└── salida/                # Se genera al ejecutar el notebook
    ├── corpus_lematizado.txt
    ├── frecuencias.csv
    └── espacio_vectorial_3d.png
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

`libro.txt` — *El sombrero de tres picos*, de *Pedro Antonio de Alarcón*. Fuente: Project Gutenberg(https://www.gutenberg.org/).
