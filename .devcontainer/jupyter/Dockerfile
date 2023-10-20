# Usa un'immagine di base che include Octave
FROM debian:bullseye-slim

# Installa Octave
RUN apt-get update && \
    apt-get install -y octave && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Installa Jupyter Notebook e Python
RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
RUN pip3 install --upgrade pip
RUN pip3 install jupyter
RUN pip3 install octave_kernel

# Abilita l'estensione Octave per Jupyter
RUN pip3 install octave_kernel

# # Crea una cartella di lavoro
# WORKDIR /workspace

# Esponi la porta 8888 per Jupyter
EXPOSE 8888

# Avvia Jupyter Notebook all'avvio
# CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--port=8888", "--allow-root"]
