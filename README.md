# TA_138_Practicas_LTspice



Regulador de tensión serie 


1) Simple

<img width="652" height="488" alt="imagen" src="https://github.com/user-attachments/assets/7092937d-5ec9-4f03-ab59-e5c0d6b6415a" />


<img width="1352" height="567" alt="imagen" src="https://github.com/user-attachments/assets/304cff77-c9b4-48d7-99b9-cf2312bacb40" />


El regulador simple utiliza un diodo zener en inversa con el valor de tensión requerido, entre los inconvenientes se encuentran:

- Caida de 0,7 V de VBE del transistor.
- Mala regulación frente a cambios de RL y de temperatura, ya que Vo depende de VBE, R_L y beta, lo cual no es deseado.

2)Regulador en serie mejorado

<img width="654" height="548" alt="imagen" src="https://github.com/user-attachments/assets/8ff7bc31-b487-493f-86f2-6e5b065adf1a" />
<img width="1358" height="568" alt="imagen" src="https://github.com/user-attachments/assets/8a35026f-ee71-4ff6-bbd8-6140cca33ef7" />

Se forma un circuito con realimentación negativa en donde se pueden identificar los bloques realimentador f ( R1 y R2 ) , amplificador a (Q1 , Q2) y la tensión de referencia la entrada negativa. El bloque amplificador consta de un emisor común y un colector común. 

Mientras se cumpla la condicicón af > 1 , la dependencia de la salida sera respecto a R1 e R2, y no de beta.

Vo = A( Vz + VBE2 ) = 1/f ( Vz + VBE2 ) = ([R1 + R2]/[R2]) ( Vz + VBE2 ) 


3) Implementación con Amplificador operacional:

<img width="847" height="263" alt="imagen" src="https://github.com/user-attachments/assets/c290f740-9a69-48b3-9ef5-0e658b46c76c" />

<img width="611" height="426" alt="imagen" src="https://github.com/user-attachments/assets/c82c5136-b8f9-4660-85d9-b63dd32d9fac" />

<img width="1357" height="571" alt="imagen" src="https://github.com/user-attachments/assets/e16d6c67-b9b8-4cfe-83ab-f5e17c1194bb" />


 4) Regulador con amplificador diferencial

  Reemplazando el emisor común con un amplificador diferencial se disminuye aun mas el ruido, debido al rechazo del modo común y la influencia de la temperatura.

  
