Home assistant dashboard panels to take data from Helios Pool and then display on dashboard panels.

So far only done for Cheetah

<img width="1530" height="703" alt="Screenshot_20261014_203001" src="https://github.com/user-attachments/assets/2c5b2840-365c-4e0f-9540-37327b1b1c87" />

ALL COINS
---------
Edit secrets.yaml with your own wallet addresses for Cheetah, Digibyte, Bitcoin and Bitcoin Cash. Copy the relevant code into your own Home assistant secrets.yaml

CHEETAH COIN
------------
cheetah-configuration.yaml

DEFINE YOUR WORKERS:

+ block starting at line 53, enter your own worker names and numeric id's. (See below). The name and ID on lines 68 and 69. And the numeric worker id's on lines 72 and 75

<img width="698" height="372" alt="Screenshot_20261015_235119" src="https://github.com/user-attachments/assets/e38eb218-3a43-4f8c-b17d-c65fe679a835" />

+ Add code from cheetah-configuration.yaml to your Home assistant configuration.yaml in the rest: section if you have one, or create a new rest: section. Note the entries to change the timestamp go under "templates"
  
+ RESTART HOME ASSISTANT

+ The three dashboard files cheetah-1, cheetah-2 and cheetah-3 contain the yaml for dashboard entries. 

GETTING WORKER ID and NAMES
---------------------------

You can get your worker id's etc by going to the heliospool page, for instance https://stats-chta.heliospool.com/users/CGrADAcqKbEcmmPksJ5ExxU53GuBURmLCt in google chrome, then F12 to bring up the inspector. Select the Network tab, Fetch/XHR, RELOAD THE PAGE, and then viewing one of the entries with your wallet code. 

<img width="1063" height="650" alt="Screenshot_20261016_000153" src="https://github.com/user-attachments/assets/a9ab1af1-6a6f-40a3-8834-20012cd8df65" />

OTHER DATA THAT CAN BE SCRAPED
------------------------------
See also the example-helios-data.json file, which shows clearly what data the api gives

NOTE: Initial guidance on how to grab the data from heliospool and build the cards was assisted by ChatGPT. The rest is me
