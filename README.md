# 360-image-compression

## Architecture<h1>

![image](https://user-images.githubusercontent.com/52626643/130815272-5eb5c339-7eb0-4bc9-986d-ea7fcb8349e1.png)

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
![image](https://user-images.githubusercontent.com/52626643/130878759-2df22965-10fd-4343-83b5-7d8eda68222e.png)
 
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
 ## Result <h1>
  ![7l0vX](https://user-images.githubusercontent.com/52626643/130887340-5f83d223-f249-4baa-9c36-84685d80cb27.jpg)

  

  
  
  
  
  
