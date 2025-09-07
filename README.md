# Programming-Assignment-2
This second programming assignment features two problems involving NumPy. The problems are called Data Normalization and Divisible by 3. Both require implementing NumPy algorithms and test our understanding of arrays, matrices, elements, and problem-solving skills.
## 1.) Data Normalization
The Data Normalization Program enables random numbers to be Normalized. Using the formula for z - score, numbers from the 5 x 5 matrix will be normalized one by one. This ensures the dataset has a mean of zero and a standard deviation of one, making it more suitable for analysis and further applications.

    import numpy as np   #Opens the Numpy Library as np

    X = np.random.random((5,5))              #Generates random numbers in a 5 by 5 matrix

    X_Normalized = X - X.mean() / X.std()    #Formula of z-score is applied and tranferred to variable "X_Normalized"

    np.save("X_Normalized.npy",X_Normalized) #Stores the normalized 5x5 array into a .npy file for later use

    print("Original X:\n", X)                #Prints the original 5 by 5 matrix
    print("\nNormalized:\n", X_Normalized)   #Prints the normalized Matrix

## 2.) Divisible by 3 Problem
The Divisible by 3 Problem takes the squares of numbers ranging from 1 to 100 and arranges them into a 10×10 matrix. From this matrix, the program identifies and extracts all elements that are divisible by 3. These filtered values are then stored in a separate array and saved as a file for later use. 

    import num py as np                #Opens the Numpy Library as np

    numbers = np.arange(1,101)         #Generates numbers from 1 to 100
    square = numbers ** 2              #Squares all the numbers from 1 to 100

    A = square.reshape(10,10)          #Forms a 10 x 10 matrix with the first 100 numbers squared

    div_by_3 = A[A % 3 == 0]           #Checks every number if divisible by 3 and stores the values at variable div_by_3

    np.save("div_by_3.npy",div_by_3)   #Saves the divisible by 3 matrix to a .npy file

    print("10 x 10 Matrix:\n", A)      #Prints 10 x 10 Matrix with first 100 positive integers squared
    print("\nElements divisible by 3:\n", div_by_3)   #Prints the matrix with numbers divisible by 3 from the original
