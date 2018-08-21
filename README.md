# Masters_Datascience_Assiagnment_5
Masters_Datascience_Assiagnment-5Masters_Datascience_Assiagnment_5

#1) Write a function to compute 5/0 and use try/except to catch the exceptions.

class zerodevider():
    def __init__(self, numerator, denominator):
        self.numerator=numerator
        self.denominator=denominator
    
    def compute(self):
        try:
            self.result= self.numerator/self.denominator
            return self.result
        except ZeroDivisionError as e:
            print('Devided by Zero caused the error')
            return "Devided by Zero Error"
        except Exception as e:
            print('Other Errors ',e)

try:
    userNumerator=int(input('Enter Numerator Value in number :'))
    userDenominator=int(input('Enter Denominator Value in number :'))
    
    ObjZeroDevider=zerodevider(userNumerator,userDenominator)
    
    result=ObjZeroDevider.compute()
    print('Result for passing 5/0 :',result)
    
except ValueError as err:
    print ('Enter Valid Integer Number')
    
except Exception as err:
    print ('Other errors ',err)

# 2. Implement a Python program to generate all sentences where subject is in ["Americans","Indians"] and verb is in ["Play", "watch"] and the object is in ["Baseball","cricket"].Hint: Subject,Verb and Object should be declared in the program as shown below.subjects=["Americans ","Indians"]verbs=["play","watch"]objects=["Baseball","Cricket"]
# Output should come as below:
# Americans play Baseball.
#Americans play Cricket.
#Americans watch Baseball.
#Americans watch Cricket.
#Indians play Baseball.
#Indians play Cricket.
#Indians watch Baseball.
#Indians watch Cricket.

try:
    subjects=["Americans ","Indians"]
    verbs=["play","watch"]
    objects=["Baseball","Cricket"]
    
    print ('Subject List: ',subjects)
    print ('verbs List: ',verbs)
    print ('objects List: ',objects)
    print('      ')
    
    print('Generated Sentences using above lists are: ')
    print('      ')
    
    
    for sub in subjects:
        for verb in verbs:
            for obj in objects:
                print(sub +' '+verb+' '+ obj)
except Exception as e:
    print('Other error. And error is',e )
