# Python-Appending-all-strings-with-required-keyword-from-to-xlsx-csv
Python:Appending all strings with required keyword +acquiring data above a range from&amp;to xlsx/csv using Jupyter Notebook (Pandas Dataframe)
## CODE



import pandas as pd


# In[28]:

//Specify the directory
df=pd.read_excel("C:\Users\Administrator\Desktop\InputFile.xlsx")


# In[8]:

//Preview of top 5 row&columns
df.head()


# In[11]:

//Name ur excel or csv files column -x1 ,x2 ...so on
//To search data in 1st column we take x1 and filling all NaN with 0
Prdata=df['x1'].fillna(0)


# In[12]:

//Previewing data from x1 without Nan
Prdata.head()


# In[23]:

//Use Fn to get boolean values and fill all NaN with False
trvals=Prdata.str.contains(" //Ur Keyword").fillna(False)


# In[25]:

//Getting all data values as required 
Final=Prdata[trvals]


# In[26]:

//Saving and writing the given dataframe to the required Excel file-
//Enter the directory
Final.to_excel("C:\Users\Administrator\Desktop\Name.xlsx")

# Our String query is done and now and We want data above a range so we write a code
# In[34]:


df.head()
arval=df['x2']


# In[55]:


Area=df['x2'].where(df['x2'] <= 1).dropna()


# In[59]:


Area.to_excel("C:\Users\Administrator\Desktop\Newvals.xlsx")
