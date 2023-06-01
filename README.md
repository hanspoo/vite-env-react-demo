# vite-env-react-demo

There is an issue when using environment variables with react and vite. The fact is that the location of the environment file is important, and the nx documentation doesn't say that. Sad is to say that the need to change prefix from NX* to VITE* is very unfortunate, because creates incompatibility and portability issues.

This is a nx repo integrated with and sole react app called app1, we have the env file _.env.development_ with content:

```
VITE_REACT1=Hello world development
```

If i put the file .env.development in:

Project Root
= doesn't work

Project Folder
= Works

Try this, start the app with:

```
nx serve app1
```

go to
http://localhost:4200/

You will see the variable empty.

Move the file .env.development to the app folder:

```
mv .env.development apps/app1/
```

And it will work !

Hope it helps.
