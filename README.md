Home assistant dashboard panels to take data from Helios Pool and then display on dashboard panels.

So far only done for Cheetah

<img width="1530" height="703" alt="Screenshot_20261014_203001" src="https://github.com/user-attachments/assets/2c5b2840-365c-4e0f-9540-37327b1b1c87" />

CHEETAH COIN
------------
cheetah-configuration.yaml
+ put in your own wallet address on line 7
+ block starting at line 53, enter your own worker names and numeric id's. (See below)
+ Add code from cheetah-configuration.yaml to your Home assistant configuration.yaml in the rest: section if you have one, or create a new rest: section
+ RESTART HOME ASSISTANT
+ The three dashboard files cheetah-1, cheetah-2 and cheetah-3 contain the yaml for dashboard entries. 

GETTING WORKER ID's
-------------------

You can get your worker id's etc by going to the heliospool page, for instance https://stats-chta.heliospool.com/users/CGrADAcqKbEcmmPksJ5ExxU53GuBURmLCt in google chrome, then F12 to bring up the inspector. Select the Network tab, Fetch/XHR, RELOAD THE PAGE, and then viewing one of the entries with your wallet code. 

<img width="1623" height="684" alt="Screenshot_20261014_180114" src="https://github.com/user-attachments/assets/c8eccccd-16cb-483a-9557-6fa550111eed" />

See also the example-helios-data.json file, which shows clearly what data the api gives

NOTE: Initial guidance on how to grab the data from heliospool and build the cards was assisted by ChatGPT. The rest is me
