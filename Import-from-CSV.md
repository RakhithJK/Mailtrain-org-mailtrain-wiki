The example list has the following custom fields set up:

![](https://cldup.com/k_40ofOKc5.png)

The CSV that we try to import from looks like the following ("Glass is half full" and "Glass is half empty" values indicate different options for setting checked/unchecked values)

```
"First name","Last name","Email","Phone","Website","Glass is half full","Glass is half empty"
"Coty","Harris","Coty.Harris@yahoo.com","694-013-6325 x7388","https://www.google.com/search?q=test1","Yes","No"
"Mauricio","Quitzon","Mauricio53@yahoo.com","966.405.4548 x0839","https://www.google.com/search?q=test2","No","true"
"Brody","Bradtke","Brody_Bradtke37@hotmail.com","1-979-543-4229","https://www.google.com/search?q=test3","false","yes"
"Rusty","Altenwerth","Rusty_Altenwerth@yahoo.com","(374) 648-7517 x8968","https://www.google.com/search?q=test4","Yes","0"
"Tiffany","Runolfsdottir","Tiffany87@hotmail.com","808.105.1813 x577","https://www.google.com/search?q=test5","false","true"
"Neha","Emmerich","Neha87@hotmail.com","1-760-394-7586 x760","https://www.google.com/search?q=test6","","1"
```

The first thing to do once we have the import file would be selecting "Import subscribers" from the List actions menu, upload the CSV and then match the columns in CSV with list fields in Mailtrain.

![](https://cldup.com/0xPWxznh26.png)

Next start the import. The status page does not update automatically, so you might need to refresh the page a few times to see if the import is finished or not. Importing happens in the background, so you can close your browser window if it's a large import. If for whatever reason import fails or stalls (for example the Mailtrain process in the server was restarted), then you can try to restart the import. This works as long as the uploaded import file is still available in the server. If the file is gone, then you would have to start everything over.

![](https://cldup.com/kwaCn96zAj.png)

Subscriber data is merged based on email address, so if a subscriber already exists, the fields that are provided from CSV are updated but fields that exist in the server but not in CSV are not touched. So you can also create partial updates, where your CSV has only 2 columns - email address and the field you want to update.

![](https://cldup.com/UVpnLLD5rg.png)