# Use ROOT official image with a specific version for reproducibility
FROM rootproject/root:6.28.10-ubuntu22.04

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

# Default command
CMD ["/bin/bash"]
