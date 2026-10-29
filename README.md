# Normalización, lematización y vectorización de un libro

Checkpoints 3, 4 y 5 de Procesamiento de Lenguaje Natural (Hybridge).

- **Checkpoint 3: limpieza.** Pipeline de texto en español aplicado a un libro completo: carga con reparación de codificación, limpieza con regex, tokenización, eliminación de stopwords, lematización con spaCy y comparativa contra stemming de NLTK.
- **Checkpoint 4: representación vectorial.** Bag-of-Words (`CountVectorizer`) y TF-IDF (`TfidfVectorizer`) sobre las oraciones del libro, TF-IDF y similitud coseno entre capítulos, y reducción a 3D con PCA para comparar ambos espacios.
- **Checkpoint 5: semántica distribucional.** Embeddings con Word2Vec (`gensim`), comparando CBOW contra Skip-gram: palabras más cercanas, similitud entre personajes, aritmética semántica y el espacio de embeddings en 3D.

Flujo del notebook: **carga del texto → limpieza → vectorización (BoW, TF-IDF y Word2Vec)**.

## Estructura

```
├── limpieza_libro.ipynb   # Limpieza (1-8), vectorización (9-13) y Word2Vec (14-16)
├── libro.txt              # Libro a procesar
├── requirements.txt       # Dependencias congeladas
└── salida/                # Se genera al ejecutar el notebook
    ├── corpus_lematizado.txt   # Texto procesado (un párrafo lematizado por línea)
    ├── frecuencias.csv
    ├── espacio_vectorial_3d.png    # PCA 3D: BoW vs TF-IDF
    ├── similitud_capitulos.png     # Similitud coseno entre capítulos
    └── embeddings_word2vec_3d.png  # PCA 3D: Word2Vec CBOW vs Skip-gram
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
