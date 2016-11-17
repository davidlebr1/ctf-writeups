#Seizure Cipher

**Category** : Web 

**Points** : 50

**Note** : Don't Blink or you might get a seizure!

***

#Write-up
This challenge was a little fuzzy. When I opened it, it looks like a snake game or something like that.

![Challenge](https://cloud.githubusercontent.com/assets/838845/20411710/ad0552d4-acf0-11e6-98f9-5fb7b50166b6.png)

Then, I found this section in the code. I decided to decrease the radius. 

```var path=new Path.Circle({center:[0,0],radius:(....),....})```

```var path=new Path.Circle({center:[0,0],radius:(3),....})```

And I was able to see the flag blinking in the top left. 

So, the text that it was written with the little circle is :

LRGM{JKTTU_YKTYNO_VUXEMUT}

This is a rot20. From this tool : [Tools find rot](http://theblob.org/rot.cgi?text=LRGM%7BJKTTU_YKTYNO_VUXEMUT%7D)

FLAG{DENNO_SENSHI_PORYGON}
