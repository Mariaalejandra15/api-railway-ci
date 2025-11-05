# Imagen base de Python
FROM python:3.12-slim

# Establece directorio de trabajo
WORKDIR /app

# Copia todos los archivos de tu proyecto
COPY . .

# Instala las dependencias
RUN pip install --upgrade pip
RUN pip install -r requirements.txt

# Expone el puerto de la API
EXPOSE 8001

# Comando de ejecución
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8001"]
