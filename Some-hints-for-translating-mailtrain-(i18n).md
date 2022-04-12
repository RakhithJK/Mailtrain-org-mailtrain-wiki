Tutorial for **mailtrain v2**

After changing one of the language files located in `mailtrain/locales` its necessary to **rebuild** the Node.js applications for the changes to take effect.

Here's a simple script to do so (stop mailtrain v2 beforehand):

I assume you have installed mailtrain in a subfolder of your home directory `~/mailtrain`, if you have it installed in another directory just change the path below.

```bash
cd $HOME/mailtrain/client && npm run build
```

After starting mailtrain again the new language strings are being used.