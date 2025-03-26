# 🚀 **isvalid 1.6.7 - The Unkillable Fork** 🏴‍☠️

### 💀 Because Updating Code is for the Weak 💀

So, you’ve got a **10-year-old** codebase held together by duct tape, dreams, and a million custom validations? Guess what? **SAME.**

This is a **patched** fork of `isvalid@1.6.7`, which originally depended on the **infamously insecure** `merge@1.2.1`. We fixed that mess by **upgrading to `merge@2.1.1`** and removing the risky deep merge operation.

Updating to a new library? **Nah.** Refactoring millions of validations? **LOL, NO.**

If you’ve found this repo, chances are:  
✅ You’re stuck with legacy code.  
✅ You have no time, energy, or patience to rewrite everything.  
✅ You just want it to **work** without security nightmares.

**Well, congratulations!** You don’t have to choose between security and sanity. This patched version lets you keep using `isvalid` without getting wrecked by prototype pollution attacks.

---

## 🛠 **What’s Changed?**
- **🔒 Fixed the CVE in `merge@1.2.1`** by upgrading to `merge@2.1.1`
- **⚡ Removed deep merging in `lib/schema.js`**
	- **Before:**
	  ```js
      var formalizedSchema = merge(true, schema);
      ```  
	- **After:**
	  ```js
      let formalizedSchema = {};
      for (let key in schema) {
          formalizedSchema[key] = schema[key];
      }
      ```  
- **🦾 Keeps the `isvalid@1.6.7` API** (because breaking changes are evil)
- **🚀 No refactoring required** – drop it in and move on with your life

---

## 🚧 **Installation**
```sh
npm install isvalid-legacy
```

## 🤔 **Why Not Just Upgrade?**
Because:
- Your code is older than some of team mates  junior devs.
- You have **better** things to do.
- Touching this code **might summon the demons of tech debt**.

---

## 🛑 **Disclaimer**
This package is basically a **band-aid on a time bomb**. But hey, at least it's a *patched* time bomb.

🚀 **Enjoy your legacy code—safely!** 🏴‍☠️