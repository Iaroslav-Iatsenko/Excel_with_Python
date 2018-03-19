import pandas as pd
import os
os.makedirs("managers")
managers = pd.read_excel('managers_all.xlsx')
for man in managers.Manager_name.unique():
    curfile = managers.loc[managers.Manager_name==man,['Client_name','Client_phone']]
    curpath='managers/'+man+'.xlsx'
    writer = pd.ExcelWriter(curpath)
    curfile.to_excel(writer,'Sheet1', index = False)
    writer.save()
