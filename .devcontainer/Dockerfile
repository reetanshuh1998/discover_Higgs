# Use ROOT official image which includes Python and ROOT
FROM rootproject/root:latest

# Install additional packages
RUN apt-get update && apt-get install -y \
    git \
    curl \
    wget \
    vim \
    nano \
    build-essential \
    && rm -rf /var/lib/apt/lists/*

# Install Python packages for Jupyter and data analysis
RUN pip install --no-cache-dir \
    jupyter \
    jupyterlab \
    notebook \
    numpy \
    matplotlib \
    scipy \
    pandas \
    uproot \
    awkward \
    ipywidgets

# Enable Jupyter widgets extension
RUN jupyter nbextension enable --py widgetsnbextension

# Set up working directory
WORKDIR /workspace

# Expose Jupyter port
EXPOSE 8888

# Set environment variables for ROOT
ENV ROOTSYS=/usr/local
ENV PATH=$ROOTSYS/bin:$PATH
ENV LD_LIBRARY_PATH=$ROOTSYS/lib:$LD_LIBRARY_PATH
ENV PYTHONPATH=$ROOTSYS/lib:$PYTHONPATH

# Default command
CMD ["/bin/bash"]
