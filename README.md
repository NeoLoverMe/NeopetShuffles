# NeopetShuffles

code for hosting Neopets UC pet trading shuffles

Basic Info:

shuffle.py - name of this script

listings.txt - where you will have the entries copy pasted from the neoboards

hostPage.html - where the hosting page code will be written to

htmlVariables.py - the boilerplate HTML formatting I use, feel free to replace it with your own version

accepts.txt - where you will have the acceptances (and passes) copy pasted from the neoboards

Instructions

1. In your terminal, make sure you have python3 installed
2. Git clone this project
3. You will first have to manually copy paste Listings from the neoboards into the listings.txt file

```
Please have them format listings in this format, the code accepts extra
info at the end of the listing but the keywords are
Listing, the tiers (T9), and the @username

Listing:

Example - UC Plushie Gnorbu (T9)
Example2 - UC Faerie Kyrii (T3) No pass

@username
```

4. Then to run the code use the command

```
python3 shuffle.py listings.txt
```

this will write all your boilerplate HTML as well as the listings into the hostPage.html file

5. You may then copy the entirety of the hostPage.html file onto whichever Pet Page you are using to host the shuffle
6. At the end of the shuffle to track acceptances you will have to manually copy paste acceptances into the accepts.txt file
7. Then to update your hostPage.html file with acceptances you will run

```
python3 shuffle.py listings.txt accepts.txt missing
```

This will now update hostPage.html with acceptances, as well as output to the terminal the missing pets which may look something like:

```
MISSING DECISIONS ON THE FOLLOWING PETS, let me know if I missed you
 no rush

Example - UC Plushie Krawk - (T9)

```

TODO

1. Clean up Readme with nicer formatting

Examples:

a sample listing

```
Listing:

Example - UC Plushie Gnorbu (T9)

@username

Listing:

Example2 - UC Faerie Kyrii (T3) No pass

@username2
```

will output into the Listings portion

```
<br>
<br>

Example2 - UC Faerie Kyrii (T3) No pass

<br>

<br>

Example - UC Plushie Gnorbu (T9)

<br>
```

and output into the Usernames portion

```
<br>
<br>

@username2

<br>

<br>

@username

<br>
```

When you are ready to update with acceptances run the following

```
python3 shuffle.py listings.txt accepts.txt missing
```

credits to neopets user: kougras_paw_brasil! a collaborative effort as she did most of the foundation building and heavy lifting and I added bonus features here and there!
