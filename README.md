# Programming_Assingment-12


1. Write a Python program to Extract Unique values dictionary values?
sol:
dict1 = {'k1': 1, 'k2': 1, 'k3': 'hello', 'k4': 'hello', 'k5':1234}
unique_values = {i for i in dict1.values()}
unique_values
{1, 1234, 'hello'}




2. Write a Python program to find the sum of all items in a dictionary?
sol:
test_dict = {'k1' : 89,
             'k2' : 111,
             'k3' : 123,
             'k4' : 5}

sum = 0
for i in test_dict.values():
    sum +=sum + i
print("Sum of all values is : {}".format(sum))
Sum of all values is : 1407




3. Write a Python program to Merging two Dictionaries?
sol:
dict1 = { 'x': 1, 'l': 2}
dict2 = { 'k': 3, 'z': 4, 'x': 11}
# merging dict2 into dict1
for item in dict2.items():
    dict1.setdefault(item[0], item[1])
print(dict1)
{'x': 1, 'l': 2, 'k': 3, 'z': 4}




4. Write a Python program to convert key-values list to flat dictionary?
sol:
test_dict = {'month' : [1, 2, 3], 'name' : ['Jan', 'Feb', 'March']}
  
# Using dict() + zip() to convert key-values list to flat dictionary
res = dict(zip(test_dict['month'], test_dict['name']))

print("Flattened dictionary : " + str(res)) 
Flattened dictionary : {1: 'Jan', 2: 'Feb', 3: 'March'}





5. Write a Python program to insertion at the beginning in OrderedDict?
sol:
from collections import OrderedDict
  
# initialising ordered_dict
iniordered_dict = OrderedDict([('Feb', '2'), ('Mar', '3')])
  
# inserting items in starting of dict 
iniordered_dict.update({'Jan':'1'})
iniordered_dict.move_to_end('Jan', last = False)
  
# print result
print ("Ordered Dictionary after insertion : "+str(iniordered_dict))
Ordered Dictionary after insertion : OrderedDict([('Jan', '1'), ('Feb', '2'), ('Mar', '3')])




6. Write a Python program to check order of character in string using OrderedDict()?
sol:
from collections import OrderedDict 
  
def checkOrderofString(str, pattern): 
      
    # create empty OrderedDict 
    dict = OrderedDict.fromkeys(str) 
    print(dict)   
    ptrlen = 0
    for key,value in dict.items(): 
        
        if (key == pattern[ptrlen]): 
            ptrlen = ptrlen + 1
          
        # check if we have traverse complete pattern string 
        if (ptrlen == (len(pattern))):            
            return 'true'
  
    # if we come out from for loop that means order was mismatched 
    return 'false'
  

string = input("enter string : ")
pattern = input("Enter Pattern : ")
if checkOrderofString(string,pattern):
    print("Pattern matched")
else:
    print("Pattern not matched")
enter string : Programming
Enter Pattern : gram
OrderedDict([('P', None), ('r', None), ('o', None), ('g', None), ('a', None), ('m', None), ('i', None), ('n', None)])
Pattern matched




7. Write a Python program to sort Python Dictionaries by Key or Value?
sol:
a = {'k1':2, 'k2':1, 'k3':3, '4':4 ,'6':6, 'key7':7}
#this will print a sorted list of the keys
print(sorted(a.keys()))
#this will print the sorted list with items.
print(sorted(a.items()))
#a = {1:2 ,2:1 ,4:3 ,3:4 ,6:5 ,5:6 }
print(sorted(a.values()))
#this will print a sorted list of values.
['4', '6', 'k1', 'k2', 'k3', 'key7']
[('4', 4), ('6', 6), ('k1', 2), ('k2', 1), ('k3', 3), ('key7', 7)]
[1, 2, 3, 4, 6, 7]




 
