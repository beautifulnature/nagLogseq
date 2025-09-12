- astro let you store environment variables in `.env` file.
- i highly recommend you store all your API keys (both secret and public) inside this `.env` file - because you can `.gitignore` this file to prevent your API keys from being exposed to the public.
- There are 2 kinds of keys:
	- secret keys
	- public keys
- secret keys:
	- you can name secret keys anything you want. the usual convention is to use the `ALL_CAPS` case for denoting a constant.
	- ```
	  A_VERY_SECRET_KEY="A Secret Key. This must never be exposed"
	  ```
	- You can retrieve a secret key with `import.meta.env.KEY_NAME`
	- ```
	  ---
	  const key = import.meta.env.A_VERY_SECRET_KEY
	  console.log(key) // 'A Secret Key. This must never be exposed'
	  ---
	  ```
	- Secret keys can only be used inside Astro files. They cannot be used in frontend frameworks (like Svelte, React or Vue).
	- Astro enforces this rule to prevent you from accidentally exposing your secret key to the public.