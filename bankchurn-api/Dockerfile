# Imagen base
FROM python:3.12-slim

# Directorio de trabajo
WORKDIR /app

# Copiamos los archivos de la API
COPY . .

# Copiamos explícitamente el archivo .whl del modelo al mismo nivel
COPY ./model-pkg/model_abandono-0.0.1-py3-none-any.whl /app/model_abandono-0.0.1-py3-none-any.whl

# Actualizamos pip e instalamos las dependencias
RUN pip install --upgrade pip
RUN pip install /app/model_abandono-0.0.1-py3-none-any.whl
RUN pip install -r requirements.txt

# Exponemos el puerto de la API
EXPOSE 8001

# Ejecutamos el servidor FastAPI
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8001"]

