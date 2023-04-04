# Inscriptions-of-Israel-Palestine
This repository shows how dataframe (csv file) can be created from the Inscriptions of Israel/Palestine database available in the following website:<br/>
https://library.brown.edu/cds/projects/iip/info/welcome/

## Usage
1. The dataframe of all inscriptions in the IIP database is available in the excel file that can be obtained from this link:<br/>
https://github.com/daikitag/Inscriptions-of-Israel-Palestine/blob/master/Overall%20Data.xlsx<br/><br/>
This excel file contains the following features from the inscriptions:<br/>
https://github.com/daikitag/Inscriptions-of-Israel-Palestine/blob/master/features.md


2. The best way to create your database is to modify the excel file, as it includes all information about the inscriptions. However, if you are interested in creating your own database, please follow the instructions.

3. If you are new to Anaconda, please follow the instructions in the following link:<br/>
https://github.com/daikitag/Inscriptions-of-Israel-Palestine/blob/master/Download%20Anaconda.md

4. Please read the instructions about obtaining the API URL from this website:<br/>
http://cds.library.brown.edu/projects/Inscriptions/iip-api.shtml

5. Obtain the Python code from the following link. Copy and paste the code to your Jupyter notebook<br/>
https://github.com/daikitag/Inscriptions-of-Israel-Palestine/blob/master/Dataframe%20from%20API.ipynb

6. In the URL section, type your own URL from the API (Blue line in the figure below). Here, do not delete the quotation marks that surround the URL.
7. If more than 5000 inscriptions appear in the API link, change the number in the "for i in range(0,5000)" to a higher number.<br/>
(Yellow line in the figure below):<br/>

![image](https://user-images.githubusercontent.com/48062118/62135257-e6a36680-b2af-11e9-85be-c1009e90d0e4.png)

8. By running the code by pressing "Ctrl" + "Enter", you can create a csv file named "summary.csv" that lists all inscriptions in the database with the features.<br/>
If you would like to change the directory of the file, put the following code in front, and type your desired directory name inside the quotation marks:<br/>
```python
import os

# Here, choose your own directory that you want to save your document
os.chdir(r'')
```

9. There are some features that cannot be obtained from the API link. The list of these features are included in the following link:<br/>
https://github.com/daikitag/Inscriptions-of-Israel-Palestine/blob/master/features.md<br/>
For these features, you must obtain them from "https://library.brown.edu/cds/projects/iip/view_xml/" + "IIP ID" link. Detailed instructions about how to use this link is summarized in the website about API. <br/>

10. If you would like to obtain a dataframe for one inscription, use the following code:<br/>
https://github.com/daikitag/Inscriptions-of-Israel-Palestine/blob/master/Dataframe%20from%20single%20file.ipynb
11. As before, change the URL <br/>
![image](https://user-images.githubusercontent.com/48062118/62136383-ff148080-b2b1-11e9-9bf4-ca3a30208922.png)
12. Also, change the file name of the csv file that you would like to create. This section is located at the last part of the document. Do not delete the ".csv" and quotation marks in the file name.<br/>
![image](https://user-images.githubusercontent.com/48062118/62136630-8104a980-b2b2-11e9-8dc6-d91b4913944a.png)
13. Run the code.
14. Most inscriptions are grouped together and the URL are similar. For example, akko0001~akko0100. In this case, you do not have to create csv documents for individual inscriptions. Instead, use the following code:<br/>
https://github.com/daikitag/Inscriptions-of-Israel-Palestine/blob/master/Dataframe%20for%20multiple%20inscriptions.ipynb
15. At first, change the URL. Instead of putting the original URL, just change the category name of the URL:<br/>
(Green line in the figure below)
16. Next, change the number in "for i in range(1,510)". For example, akko only has 0001~0100, so it is better to set this as range(1,101), as setting a large number wil take a longer time.
![image](https://user-images.githubusercontent.com/48062118/62137434-eefda080-b2b3-11e9-9bad-e8832e587dec.png)
17. Finally, change the name of the csv file that you would like to save. This section is at the end of the code.<br/>
![image](https://user-images.githubusercontent.com/48062118/62137857-a2669500-b2b4-11e9-9a86-3089b0f0b5c5.png)
18. Run the code.
<br/>

# Data Preprocess

After obtaining the inscription dataset, data preprocess was conducted by using the files in "Data Preprocess" folder