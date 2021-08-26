# 360-image-compression

## Architecture<h1>

![image](https://user-images.githubusercontent.com/52626643/130976944-406b5ae7-719f-45f8-9298-e40159fdc7b7.png)

Il se compose de quatre gros parties :
1. Projection stéréographique
2. Code pour générer une région d'intérêt multi-structure (MSROI) (Partie d analyse semantique en utilisant un modele CNN)
3. Compression Bit allocation algorithm 
4.  Reseau de compression basee sur un modele RNN 

Requirements:
1. Tensorflow
2. Numpy
3. Pandas
4. Python PIL
5. Python SKimage
  
Dataset : https://aliensunmin.github.io/project/360-dataset/

## 1. Projection stéréographique (La premiere etape): <h1>
  
```
  python 1.Stereographic Projection.ipynb
```
![image](https://user-images.githubusercontent.com/52626643/130977364-8aeb9217-bc3f-440b-b503-8326ed7e1baf.png) 
## 2. Réseau d'Analyse Sémantique: <h1>

 ```
  python generate_map.py <image_file>
```
 ###### La sortie est dans le fichier 'output'. <h6>
  ![image](https://user-images.githubusercontent.com/52626643/130879540-048f1cfd-6966-4ec3-8afe-c527f02ae026.png)
  
## 3. Compression Bit allocation algorithm : <h1>
```
  python Compression-bit-allocation-algo <image_file>
```
## 4. Réseau de compression: <h1>
  ![image](https://user-images.githubusercontent.com/52626643/130880870-8e10af0b-289c-400e-9675-a926cc73366e.png)
   ###### *Encoding* <h6>
  ```
  python encode.py --model save/model --input kodim05.png --iters 24 --output compressed.npz

  ```

  ###### *Decoding* <h6>
 ```
    python decode.py --model save/model --input compressed.npz --output compressed.png

 ```
 ## Résultat <h1>
  #### Image Originale <h4>
  ![7l0vX](https://user-images.githubusercontent.com/52626643/130887340-5f83d223-f249-4baa-9c36-84685d80cb27.jpg)
 #### Image compressée <h4>

![image](https://user-images.githubusercontent.com/52626643/130976555-ac98e33a-9a8e-4420-b8b3-46dda0c185be.png)

  

  
  
  
  
  
