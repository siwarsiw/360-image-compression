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

How to use this code ?

