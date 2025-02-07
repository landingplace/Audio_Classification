Device: Thingy53

![image](https://github.com/user-attachments/assets/98e11c20-90e2-4660-b2f4-91cbdf60e6fc)


* Collect Data: 

1) click mouse left key: MOUSE-L

2) click mouse right key: MOUSE-R

3) click "A" on keyboard: KB-A

4) click "J" on keyboard: KB-J

5) click "enter" key on keyboard: KB-ENT

Training set: x50

Testing set: x13

![image](https://github.com/user-attachments/assets/e47e760e-f9ef-4512-bb86-41df68874fbc)


* Create Impulse: 

- Processing block: Audio (MFCC)

- learning block: Classification

* MFCC: 

![image](https://github.com/user-attachments/assets/8b00088a-e19e-488b-b987-2c29396261b6)

* Classifier: 

- Training settings: 

          > Number of training cycles: 100

          > Learning rate: 0.005

          > Training processor: CPU
![image](https://github.com/user-attachments/assets/4999c6f4-b9b5-4b7f-8cc9-d3592130bc5e)


=> Training Output: 

![image](https://github.com/user-attachments/assets/df3ae344-3f4a-41a7-8f66-f40d85b8d6cc)

![image](https://github.com/user-attachments/assets/1aa43145-5dac-4194-a8d1-d2f6acd4a4b8)

* Model testing:
  
![image](https://github.com/user-attachments/assets/8233b527-6c67-4c8c-8b62-8f025b10a1a1)

![image](https://github.com/user-attachments/assets/9ae021ec-c63c-465b-b5ec-7902f10e2f3f)

![image](https://github.com/user-attachments/assets/966771ae-4d5b-4aa7-87d3-646772cb4be0)






* Deployment: 

   - Compiler: EON

   - Quantized: int8

1) Run model in browser: use phone to scan the 3D barcode

![image](https://github.com/user-attachments/assets/79dc84f2-7b06-481b-990b-3ce4a64dd83a)

output: 

![image](https://github.com/user-attachments/assets/bce18b96-0ed4-43e9-a343-4eff248ad0c3)

2) Deploy on Thingy53 with the ".zip" file

output: 

![image](https://github.com/user-attachments/assets/18370414-f34e-42e5-bb51-cc8f5f415c00)

* Discussion: 

The "Spectrogram" processing block was used. The accuracy is very low: 

1)  Number of training cycles: 100 /Learning rate: 0.005    

![image](https://github.com/user-attachments/assets/0d77a740-75bb-4856-b4dd-dc1c8b773835)

2)  Number of training cycles: 100 / Learning rate: 0.0005    

![image](https://github.com/user-attachments/assets/4eeed870-7be3-4b4d-9394-f6f90017d05d)

3)  Number of training cycles: 200 / Learning rate: 0.0005    

![image](https://github.com/user-attachments/assets/daff04a0-eee6-4774-9f3d-ce5d5de542b3)

4)  Number of training cycles: 300 / Learning rate: 0.0005    

![image](https://github.com/user-attachments/assets/55d6f3b3-d2ec-4d98-a49c-6e8637c98b07)

We can see with the number of training cycles increasing, the accuracy improved until a certain turning point. 

Overall, the Audio MFCC processing is performing much better than the Spectrogram processing block. 
