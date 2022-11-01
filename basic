#!/usr/bin/env python
# coding: utf-8

# In[6]:


"""Write a python program to display all the common characters between two strings. 
Return -1 if there are no matching characters.
Note: Ignore blank spaces if there are any. Perform case sensitive string comparison wherever necessary.

Sample Input
"I like Python"
"Java is a very popular language"

Expected output
lieyon"""
def find_common_characters(msg1,msg2):
    list=[]
    for x in msg1:
        if x==" ":
            continue
        else:
            for y in msg2:
                if x == " ":
                    continue
                elif x == y:
                    if x in list:
                        break
                    else:
                        list.append(x)
                        break
    output="".join(list)
    if len(output)==0:
        return -1
    else:
        return output
#Provide different values for msg1,msg2 and test your program
msg1="moto"
msg2="moto"
common_characters=find_common_characters(msg1,msg2)
print(common_characters)


# In[ ]:



"""Write a python function, encrypt_sentence() which accepts a message and encrypts it based on rules given below
and returns the encrypted message.

Words at odd position -> Reverse It
Words at even position -> Rearrange the characters so that all consonants appear before the vowels
and their order should not change

Note: 
Assume that the sentence would begin with a word and there will be only a single space between the words.
Perform case sensitive string operations wherever necessary.
Sample Input
the sun rises in the east
Expected Output
eht snu sesir ni eht stea"""

vowels=['a','e','i','o','u']

def encrypt_sentence(sentence):
    final=[]
    list_sentence = sentence.split(" ")
    for index,word in enumerate(list_sentence):
        if (index+1)%2!=0:
            final.append(word[::-1])
        else:
            v=[]#to store all vowels
            t=[]#to store the letters temporily
            for letter in word:
                if letter not in vowels:
                    t.append(letter)
                else:
                    v.append(letter)
            t.extend(v)
            final.append("".join(t))
    #if len(final)>1:
    return " ".join(final)
                    
sentence="the"
encrypted_sentence=encrypt_sentence(sentence)
print(encrypted_sentence)
sentence="hello i am omkar"
encrypted_sentence=encrypt_sentence(sentence)
print(encrypted_sentence)


# In[ ]:


"""Write a python function, find_correct() which accepts a dictionary and returns a list as per the rules mentioned below.
The input dictionary will contain correct spelling of a word as key and the spelling provided by a contestant as the value.

The function should identify the degree of correctness as mentioned below:
CORRECT, if it is an exact match

ALMOST CORRECT, if no more than 2 letters are wrong
WRONG, if more than 2 letters are wrong or if length (correct spelling versus spelling given by contestant) mismatches.

and return a list containing the number of CORRECT answers, number of ALMOST CORRECT answers and number of WRONG answers. 
Assume that the words contain only uppercase letters and the maximum word length is 10.

Sample Input
{"THEIR": "THEIR", "BUSINESS": "BISINESS","WINDOWS":"WINDMILL","WERE":"WEAR","SAMPLE":"SAMPLE"}

Expected Output
[2, 2, 1]"""
def find_correct(word_dict):
    #start writing your code here
    key=[]
    value=[]
    count=0
    correct=0
    wrong=0
    atmost=0
    result=[]
    for i,j in word_dict.items():
            key.append(i)
            value.append(j)
    for i in range(len(key)):
        if(len(key[i])==len(value[i]) and key[i]==value[i]):
            correct+=1
        elif((len(key[i])==len(value[i]))==False):
            wrong+=1
        else:
            for j in range(len(key[i])):
                if((key[i][j]==value[i][j])==False):
                    count+=1
                    if(count>2):
                        wrong+=1
                        break
            if(count<=2):
                atmost+=1
            count=0
           
           
    result=[correct,atmost,wrong]
    return result
       


word_dict={"THEIR": "THEIR","BUSINESS":"BISINESS","WINDOWS":"WINDMILL","WERE":"WEAR","SAMPLE":"SAMPLE"}
print(find_correct(word_dict))


# In[7]:


# Care hospital wants to know the medical speciality visited by the maximum number of patients.
Assume that the patient id of the patient along with the medical speciality visited by the patient is stored in a list. 
The details of the medical specialities are stored in a dictionary as follows:
# {
# "P":"Pediatrics",
# "O":"Orthopedics",
# "E":"ENT
# } 

# Write a function to find the medical speciality visited by the maximum number of patients 
and return the name of the speciality.
# Also write the pytest test cases to test the program.
"""Sample Input AND Expected Output

[101,P,102,O,302,P,305,P]

Pediatrics

[101,O,102,O,302,P,305,E,401,O,656,O]

Orthopedics

[101,O,102,E,302,P,305,P,401,E,656,O,987,E]

ENT"""

def max_visited_speciality(patient_medical_speciality_list,medical_speciality):
   
    result = [0,0,0]
    i = 1 
    while(i< len(patient_medical_speciality_list)):
        if patient_medical_speciality_list[i] == 'P': result[0] = result[0] + 1
        elif patient_medical_speciality_list[i] == 'O' : result[1] = result[1] + 1
        else : result[2] = result[2] + 1
        i = i + 2
    a = max(result)
    a = result.index(a)
    if a == 0: speciality = 'Pediatrics'
    elif a == 1: speciality ='Orthopedics'
    else : speciality = 'ENT'

    return speciality


patient_medical_speciality_list=[301,'O',302, 'P' ,305, 'P' ,401, 'E' ,656, 'E']
medical_speciality={"P":"Pediatrics","O":"Orthopedics","E":"ENT"}
speciality=max_visited_speciality(patient_medical_speciality_list,medical_speciality)
print(speciality)


# In[9]:


"""Write python function, sms_encoding() which accepts a sentence and converts it into an abbreviated sentence to be sent as SMS and returns the abbreviated sentence. 

Rules are as follows: 
a. Spaces are to be retained as is 
b. Each word should be encoded separately

If a word has only vowels then retain the word as is

If a word has a consonant (at least 1) then retain only those consonants

Note: Assume that the sentence would begin with a word and there will be only a single space between the words.

Sample Input ANDExpected Output

I love Python
I lv Pythn

MSD says I love cricket and tennis too
MSD sys I lv crckt nd tnns t

I will not repeat mistakes
I wll nt rpt mstks"""

def sms_encoding(data):
    word=data.split()
    vowels="aeiouAEIOU"
    st=""
    for i in word:
        if(len(i)==1):
            st=st+i
        else:
            for j in i:
                if j not in set(vowels):
                    st=st+j
        st=st+" "
    return st[0:-1]
data="I love Python"
print(sms_encoding(data))


# In[12]:


"""Write a python program that accepts a text and displays a string which contains the word with the largest frequency 
in the text and the frequency itself separated by a space.

Rules:

The word should have the largest frequency.

In case multiple words have the same frequency, then choose the word that has the maximum length.

Assumptions:

The text has no special characters other than space.

The text would begin with a word and there will be only a single space between the words.

Perform case insensitive string comparisons wherever necessary.
Sample Input and Expected Output

"Work like you do not need money love like you have never been hurt and dance like no one is watching"
like 3

"Courage is not the absence of fear but rather the judgement that something else is more important than fear"
fear 2"""
def max_frequency_word_counter(data):
    word=""
    frequency=0
    lower_data=data.lower()
    lst=[]
    lst=lower_data.split()
    repeat=[]
    a=[]
    i=0
    while(i < len(lst)):
        if lst.count(lst[i]) > 1:
            repeat.append(lst[i])
            i=i+1
        else:
            i=i+1
    for i in repeat:
        a=repeat.count(i)
    
    for i in range(0,len(repeat)):
        if repeat.count(repeat[i])==a:
            word=word+repeat[i]
            frequency=a
            break
    print(word,frequency)


#Provide different values for data and test your program.
data="Work like you do not need money love like you have never been hurt and dance like no one is watching"
max_frequency_word_counter(data)


# In[1]:


sample_dict = {'a':1,'b':2}
sample_dict.update({'b':5, 'c':10 })
print(sample_dict.get('b'), sample_dict.get('c'))
 


# In[4]:


my_library ={103 : "Alice in Wonderland",104 : "The Turning Point",113 : "Wings on Fire",134 : "Harry Potter"}
print(my_library[104])


# In[5]:


listA = [1,2,3,4,5,5,6,6,7,7,7,8,8,8,8] 
print(set(listA))


# In[ ]:




