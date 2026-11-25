# TP4 - Redes convolucionales para clasificar lesiones de piel (ISIC)

Trabajo práctico de Redes Neuronales. Clasificación de imágenes dermatoscópicas del dataset ISIC (9 clases, unas 880 imágenes) con una red convolucional, comparada contra una MLP. El código viene del notebook de la materia, y el trabajo es ejecutarlo, explicar el código convolucional y analizar los resultados (exploración del dataset, MLP contra CNN, decisiones de arquitectura, data augmentation y evaluación final en test).

## Qué hay en el repo

- `CNN_en_Skin_Dataset.ipynb` es el notebook ejecutado de punta a punta, con todos los outputs y las celdas de análisis completas.
- `requirements.txt` tiene las librerías con las versiones que usé.

El dataset no está en el repo.

## Cómo reproducirlo

1. Clonar este repo y, dentro de la carpeta, copiar la carpeta `data/Split_smol` del repo de la materia ([cselmo/CNN-en-Skin-Dataset](https://github.com/cselmo/CNN-en-Skin-Dataset)), de forma que quede `data/Split_smol/train` y `data/Split_smol/val`, con una subcarpeta por clase.
2. Instalar las dependencias y abrir el notebook desde la carpeta que contiene `data/`.

```bash
python -m venv .venv
source .venv/bin/activate        # en Windows .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook CNN_en_Skin_Dataset.ipynb
```

3. Ejecutar todas las celdas en orden. No cambié ninguna de las constantes de la sección 0, así que con la misma semilla de split los conjuntos de train, validación y test son los mismos. Yo lo corrí en CPU con 2 hilos y tardó unos 25 minutos. Los tiempos que aparecen en el notebook dependen de eso.
