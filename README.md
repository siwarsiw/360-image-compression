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

## 1. Projection stéréographique (La premiere etape): <h1>
  
```
  python 1.Stereographic Projection.ipynb
```
 Input :
 ![7fB65](https://user-images.githubusercontent.com/52626643/130878082-6fed98e1-d5b1-463d-98ee-7d508a59d72d.jpg)
 Output :
![split_0_2](https://user-images.githubusercontent.com/52626643/130878144-23be5f23-8683-473b-b89e-d5bca3a339ca.jpg)
![split_1_2](https://user-images.githubusercontent.com/52626643/130878149-2c472032-efee-4931-a5dd-8cca8a2ec3f8.jpg)
![split_2_2](https://user-images.githubusercontent.com/52626643/130878151-02b3ca2c-c8df-41c8-b72d-3c5a403c039e.jpg)
![split_3_2](https://user-images.githubusercontent.com/52626643/130878153-ad8cb9bb-f379-43df-8a7f-c3114d614335.jpg)


  
  
  
  
  
  
