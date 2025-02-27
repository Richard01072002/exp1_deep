# EXP-1
### Name- RICHARDSON A
### reg no. - 212222233005
### dep - AI & DS 
## AIM
#### To understand and demonstrate the conversion of NumPy arrays into PyTorch tensors and explore various ways to create tensors in PyTorch.
## procedure 
#### Step 1: Install OpenCV
#### Step 2: Check PyTorch Version
#### Step 3: Create a NumPy array and print its type and data type.
#### Step 4: Create a 2D NumPy array and reshape it and Convert it to a PyTorch tensor and print the results.
#### Step 5: Modify the original NumPy array and observe changes in the tensor when using torch.from_numpy().
#### Step 6: Create PyTorch Tensors Using Different Methods:
#### Step 7: Use torch.Tensor(data) to create a tensor. Use torch.tensor(data) to create a tensor with the default type.
#### Step 8: Create an uninitialized tensor with torch.empty().Create a zero tensor using torch.zeros().
#### Step 9: Generate a tensor with evenly spaced values using torch.arange().Create a tensor using torch.linspace() for equally spaced values.

## program
```
import torch
import numpy as np
orch.__version__
```
#### output 1
<img width="166" alt="Screenshot 2025-02-27 at 2 11 30 PM" src="https://github.com/user-attachments/assets/261eb803-aed0-4f74-ae1d-58876bdf8b0b" />



```
arr = np.array([1,2,3,4,5])
print(arr)
print(arr.dtype)
print(type(arr))
```
#### output 2
<img width="212" alt="Screenshot 2025-02-27 at 2 12 21 PM" src="https://github.com/user-attachments/assets/08373bfa-0076-459e-aab3-300593d333b3" />




```
x = torch.from_numpy(arr)
# Equivalent to x = torch.as_tensor(arr)
print(x)
```
#### output 3
<img width="162" alt="Screenshot 2025-02-27 at 2 12 42 PM" src="https://github.com/user-attachments/assets/ca65f180-7bf3-4074-9aca-4c4b774096de" />




```
# Print the type of data held by the tensor
print(x.dtype)
```
#### output 4
<img width="146" alt="Screenshot 2025-02-27 at 2 13 03 PM" src="https://github.com/user-attachments/assets/9182e13a-0633-42bc-a0aa-f27f39befca9" />


```
print(type(x))
print(x.type())
```
#### output 5
<img width="218" alt="Screenshot 2025-02-27 at 2 13 34 PM" src="https://github.com/user-attachments/assets/844f8e43-b111-407b-be3f-a0f7ad634a73" />


```
arr2 = np.arange(0.,12.).reshape(4,3)
print(arr2)
```
#### output 6
<img width="172" alt="Screenshot 2025-02-27 at 2 13 57 PM" src="https://github.com/user-attachments/assets/385dc7aa-58fe-4580-b3e4-3997b695ee84" />


```
x2 = torch.from_numpy(arr2)
print(x2)
print(x2.type())
```
#### output 7
<img width="421" alt="Screenshot 2025-02-27 at 2 14 35 PM" src="https://github.com/user-attachments/assets/bd88cfdc-8472-46cc-b664-9174468ab333" />


```
arr = np.arange(0,5)
t = torch.from_numpy(arr)
print(t)
```
#### output 8
<img width="290" alt="Screenshot 2025-02-27 at 2 15 23 PM" src="https://github.com/user-attachments/assets/b5ca9f3c-6fd7-4dba-b284-b37c46000aa9" />



```
arr[2]=77
print(t)
```
#### output 9
<img width="288" alt="Screenshot 2025-02-27 at 2 15 49 PM" src="https://github.com/user-attachments/assets/fb05a1a2-75ac-44b5-8009-85eab3a1b69d" />



```
# Using torch.tensor()
arr = np.arange(0,5)
t = torch.tensor(arr)
print(t)
```
#### output 10
<img width="219" alt="Screenshot 2025-02-27 at 2 16 29 PM" src="https://github.com/user-attachments/assets/160d6456-c3a0-4ae1-911a-f5192f1a0187" />




```
arr[2]=77
print(t)
```
#### output 11
<img width="234" alt="Screenshot 2025-02-27 at 2 16 44 PM" src="https://github.com/user-attachments/assets/e07b884c-910e-4437-920c-78b939ee4723" />




```
data = np.array([1,2,3])
```

```
a = torch.Tensor(data)  # Equivalent to cc = torch.FloatTensor(data)
print(a, a.type())
```
#### output 13
<img width="369" alt="Screenshot 2025-02-27 at 2 17 32 PM" src="https://github.com/user-attachments/assets/43ba2ddc-935c-4dba-8b2a-58c9714c4799" />


```
b = torch.tensor(data)
print(b, b.type())
```
#### output 14
<img width="338" alt="Screenshot 2025-02-27 at 2 18 07 PM" src="https://github.com/user-attachments/assets/eac40b69-b11b-4513-92d1-fd64503abe05" />




```
x = torch.empty(4, 3)
print(x)
```
#### output 15
<img width="323" alt="Screenshot 2025-02-27 at 2 18 21 PM" src="https://github.com/user-attachments/assets/df8bf206-6e24-4a1c-aff8-673430094395" />



```
x = torch.zeros(4, 3, dtype=torch.int64)
print(x)
```
#### output 16
<img width="453" alt="Screenshot 2025-02-27 at 2 18 43 PM" src="https://github.com/user-attachments/assets/0129651e-0f9a-4c27-aa89-9027da5e52bd" />




```
x = torch.arange(0,18,2).reshape(3,3)
print(x)
```
#### output 17
<img width="257" alt="Screenshot 2025-02-27 at 2 18 54 PM" src="https://github.com/user-attachments/assets/6bf57755-8d29-49e4-8b09-38969d5be85d" />




```
x = torch.linspace(0,18,12).reshape(3,4)
print(x)
```
#### output 18
<img width="432" alt="Screenshot 2025-02-27 at 2 19 57 PM" src="https://github.com/user-attachments/assets/1d8cab46-de5a-4bd6-9991-2f3c10aa3991" />





```
x = torch.tensor([1, 2, 3, 4])
print(x)
print(x.dtype)
print(x.type())
```
#### output 19
<img width="193" alt="Screenshot 2025-02-27 at 2 20 17 PM" src="https://github.com/user-attachments/assets/0bf657d7-0460-4c51-8843-5f5247d7ff3a" />



```
x = torch.FloatTensor([5,6,7])
print(x)
print(x.dtype)
print(x.type())
```
#### output 20
<img width="186" alt="Screenshot 2025-02-27 at 2 20 34 PM" src="https://github.com/user-attachments/assets/789c2903-fc58-4eb7-b9d5-f5ded55be464" />



```
x = torch.tensor([8,9,-3], dtype=torch.int)
print(x)
print(x.dtype)
print(x.type())
```
#### output 21
<img width="364" alt="Screenshot 2025-02-27 at 2 20 53 PM" src="https://github.com/user-attachments/assets/9dd55563-6bfc-4ae5-be5b-2281c45194ed" />



```
print('Old:', x.type())
x = x.type(torch.int64)
print('New:', x.type())
```
#### output 22
<img width="255" alt="Screenshot 2025-02-27 at 2 21 12 PM" src="https://github.com/user-attachments/assets/096fd079-779d-468d-b0d4-2771c512b860" />



```
x = torch.rand(4, 3)
print(x)
```
#### output 23
<img width="367" alt="Screenshot 2025-02-27 at 2 21 35 PM" src="https://github.com/user-attachments/assets/17736ebc-d81f-45da-8a2a-369be7b74aa4" />



```
x = torch.randn(4, 3)
print(x)
```
#### output 24
<img width="351" alt="Screenshot 2025-02-27 at 2 21 50 PM" src="https://github.com/user-attachments/assets/3f851c65-921b-4434-8925-8abfabc8e93f" />



```
x = torch.randint(0, 5, (4, 3))
print(x)
```
#### output 25
<img width="230" alt="Screenshot 2025-02-27 at 2 22 24 PM" src="https://github.com/user-attachments/assets/555560be-c526-4f7f-a184-2322ca9a94a7" />




```
x = torch.zeros(2,5)
print(x)
```
#### output 26
<img width="284" alt="Screenshot 2025-02-27 at 2 23 19 PM" src="https://github.com/user-attachments/assets/bb53296f-15a4-4dc8-a577-152814acb047" />



```
x2 = torch.randn_like(x)
print(x2)
```
#### output 27
<img width="504" alt="Screenshot 2025-02-27 at 2 23 44 PM" src="https://github.com/user-attachments/assets/cd7cd456-7fb4-4abc-a369-2e0438a7dd8f" />



```
x3 = torch.ones_like(x2)
print(x3)
```
#### output 28

<img width="273" alt="Screenshot 2025-02-27 at 2 29 38 PM" src="https://github.com/user-attachments/assets/c12c257e-2a53-412b-a4a6-52170e9197f3" />




```
torch.manual_seed(42)
x = torch.rand(2, 3)
print(x)
```
#### output 29

<img width="347" alt="Screenshot 2025-02-27 at 2 29 49 PM" src="https://github.com/user-attachments/assets/1cf16065-9f51-44d2-a342-481cba4c2485" />



```
x.shape
```
#### output 30
<img width="263" alt="Screenshot 2025-02-27 at 2 30 04 PM" src="https://github.com/user-attachments/assets/88f53d55-4ebd-4f3f-af3d-51b3d199c552" />


### Result 
#### Successfully created and manipulated PyTorch tensors from NumPy arrays. Understood the difference between torch.tensor() and torch.from_numpy(). Learned how PyTorch tensors share memory with NumPy arrays when using from_numpy(). Demonstrated various ways to create tensors using PyTorch functions like empty(), zeros(), arange(), and linspace().


