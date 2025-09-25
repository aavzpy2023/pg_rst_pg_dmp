# Usar una imagen base de NVIDIA con CUDA
FROM docker.io/nvidia/cuda:12.1.0-devel-ubuntu22.04

# Instalar dependencias necesarias para la detección de hardware y la instalación
RUN apt-get update && apt-get install -y curl pciutils && rm -rf /var/lib/apt/lists/*

# Descargar e instalar Ollama usando el script oficial
RUN curl -fsSL https://ollama.com/install.sh | sh

EXPOSE 11434

CMD ["/usr/local/bin/ollama", "serve"]
