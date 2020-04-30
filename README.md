# AMR_semantic_segmentation
Implementation of semantic segmentation for an AMR

This repository uses the [FCHarDNet](https://github.com/PingoLH/FCHarDNet) implementation from this [repo](https://github.com/omarsayed7/Road-Scene-Segmentation).

# Run
1. Install Docker following the instructions on the [link](https://docs.docker.com/engine/install/ubuntu/).
2. Open a terminal

3. Clone this repository and go to the folder
    ```bash
    git clone https://github.com/jdgalviss/AMR_semantic_segmentation.git
    cd AMR_semantic_segmentation
    ```
4. Build the docker container (this may take several minutes)
    ```bash
    docker build . -t segmentation
    ```
5. Run the docker container. This will enable a terminal inside the container.
    ```bash
    docker run -p 8888:8888 -it --rm --gpus all segmentation
    ```
6. Inside container, run jupyter lab
    ```bash
    jupyter lab --ip=0.0.0.0 --port=8888 --allow-root
    ```
6. Open the notebook FCHarDNet/warp_scan_segmentation.ipynb
