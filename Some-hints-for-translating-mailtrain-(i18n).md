Tutorial for **mailtrain v2**

After changing one of the language files located in `mailtrain/locales` its necessary to **rebuild** the Node.js applications for the changes to take effect.

Here's a simple script to do so:

I assume you have installed mailtrain in a subfolder of your home directory `~/mailtrain`, if you have it installed in another directory just change the path below.

```bash
cd $HOME/mailtrain/client && npm run build
```

After rebuilding the application the new language strings are being used.