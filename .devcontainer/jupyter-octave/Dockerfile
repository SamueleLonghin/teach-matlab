FROM python:3.12.0

# Preparo per utilizzare il kernel
# RUN pip install cairosvg 
# RUN pip install metakernel 
# RUN apt-get install libpangocairo-1.0-0


# Installa Octave
RUN apt-get update && \
    apt-get install -y octave && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# RUN apt-get update && apt-get install gnuplot 
#&& apt-get install gnuplotx-11


# Installa Jupyter
RUN apt-get update 
RUN pip3 install --upgrade pip
RUN pip3 install jupyter



RUN pip install octave_kernel


# RUN touch ~/.jupyter/octave_kernel_config.py
# RUN echo "c.OctaveKernel.plot_settings = dict(backend='qt')" > ~/.jupyter/octave_kernel_config.py


# Clono il kernel
# RUN git clone https://github.com/samuelelonghin/jupyter-gpp-kernel.git /usr/local/share/jupyter/kernels/jupyter-gpp-kernel

# Copio kernel
# COPY ./jupyter-gpp-kernel /usr/local/share/jupyter/kernels/jupyter-gpp-kernel


# Abilita l'estensione GPP Octave per Jupyter
# RUN jupyter kernelspec install --user /usr/local/share/jupyter/kernels/jupyter-gpp-kernel
# RUN jupyter kernelspec install --user .devcontainer/jupyter\ cool/jupyter-gpp-kernel
# RUN export PYTHONPATH="~/.local/share/jupyter/kernels:${PYTHONPATH}"

# Aggiungo la cartella con i kernel alla path di python. In questo modo troverà il modulo del kernel
ENV PYTHONPATH="/usr/local/share/jupyter/kernels:${PYTHONPATH}"