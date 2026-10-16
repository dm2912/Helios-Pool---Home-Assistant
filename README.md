Home Assistant dashboards and REST sensors for monitoring Helios Pool cryptocurrency mining statistics.

So far only done for Cheetah

<img width="1530" height="703" alt="Screenshot_20261014_203001" src="https://github.com/user-attachments/assets/2c5b2840-365c-4e0f-9540-37327b1b1c87" />

STEP 1. ALL COINS
-----------------
Edit secrets.example.yaml with your own wallet addresses for Cheetah, Digibyte, Bitcoin and Bitcoin Cash. Copy the relevant code into your own Home assistant secrets.yaml found in the Home Assistant Config directory. 

STEP 2. CHEETAH COIN
--------------------
cheetah-configuration.yaml

DEFINE YOUR WORKERS:

+ block starting at line 66, enter your own worker names and numeric id's. (See below). The name and ID on lines 73 and 76. And the numeric worker id's on lines 87 and 90. If you have more than two workers you can just copy/paste those blocks and remember to also add the later template blocks to convert the timestamps

<img width="698" height="372" alt="Screenshot_20261015_235119" src="https://github.com/user-attachments/assets/e38eb218-3a43-4f8c-b17d-c65fe679a835" />

+ Copy the code from cheetah-configuration.yaml to your **Home assistant configuration.yaml** in the rest: section if you have one, or create a new rest: section. Note the entries to change the timestamp go under "templates"

**NOTE: IF YOU ARE ADDING MULTIPLE TEMPLATES TO YOUR CONFIGURATION.YAML ENSURE YOU SEPARATE THE "REST" AND "TEMPLATES" SECTIONS**
  
+ RESTART HOME ASSISTANT

+ The three dashboard files cheetah-1, cheetah-2 and cheetah-3 contain the yaml for dashboard entries. 

Bear in mind that in the third dashboard which is your workers, you will have to adjust it to reflect your worker names. 

<img width="1102" height="554" alt="Screenshot_20261016_001012" src="https://github.com/user-attachments/assets/7b821f15-8fa1-4ad4-824a-d37d1ce4ff65" />


STEP 2/3. OTHER COINS
---------------------

The process is exactly the same as with Cheetah Coin just using the other templates.

GETTING WORKER IDs
------------------

You can get your worker id's etc by going to the heliospool page, for instance https://stats-chta.heliospool.com/users/CGrADAcqKbEcmmPksJ5ExxU53GuBURmLCt in google chrome, then F12 to bring up the inspector. Select the Network tab, Fetch/XHR, RELOAD THE PAGE, and then viewing one of the entries with your wallet code. 

<img width="1136" height="792" alt="Screenshot_20261016_000802" src="https://github.com/user-attachments/assets/e086d159-6537-4b71-8ef4-0d67963f5436" />

OTHER DATA THAT CAN BE SCRAPED
------------------------------
See also the example-helios-data.json file, which shows clearly what data the api gives

NOTE: Initial guidance on how to grab the data from heliospool and build the cards was assisted by ChatGPT. The rest is me
