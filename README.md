## Prerrequisitos: tener instalado Python en el computador.
## Paso #1: Instalar anaconda.
- Link de  [Anaconda](https://www.anaconda.com/).

## Paso #2: Abrir la terminal de “anaconda prompt” y ejecutar los siguientes códigos:

- `conda create -n tesis Python=3.9`

- Debe aceptar todos los procesos (normalmete le piden que digite "y" o "s").

## paso #3: activar el entorno y instalar dependencias.

conda activate tesis

pip install ultralytics


## paso #4 verificar el estado de la gpu y en caso de no ser compatible usar la cpu.

python

import torch
torch.cuda.is_available()

- si el resultado es falso y usted posee una tarjeta grafica NVIDIA, necesitara instalar pytorch con Cuda por el contrario si posee una - tarjeta grafica distinta a NVIDIA o no posee una ingrese este codigo: `pip3 install --upgrade torch torchvision torchaudio`
- omita lo siguiente:

torch.__version__

exit()


- si el resultado tiene la palabra "gpu", omita el paso anterior de lo contrario dirijase a esta direccion
- https://pytorch.org/get-started/locally/
- o pegue este codigo en su terminal anaconda prompt (recuerde que esto se debe realizar solo si tiene una grafica NVIDIA:
pip3 install --upgrade torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu117
## Con esto ya configuro el entorno del proyecto.

## Paso #5: dirijirse al directorio en donde se encuentran los archivos del proyecto, por ejemplo:

`cd /Descargas/proyectotesis`

codigo de deteccion 2(imagenes): yolo task=detect mode=predict model=peso.pt source=8.jpg conf=0.5

codigo de deteccion 4 (videos):  yolo task=segment mode=predict model=peso.pt conf=0.3 source=mmm.mp4 show=True 
