---
title: 'Form Validate AV'
description: 'The Therapist Your Broken Forms Never Knew They Needed'
pubDate: 'May 01 2025'
heroImage: '/formvalidate.png'
---

# `form-validate-av`: The Therapist Your Broken Forms Never Knew They Needed


Let’s get one thing straight: your forms are a *mess*.  
Your email fields are accepting "asdf@lol", your passwords are weaker than my willpower on a Friday night, and your validation strategy is basically **"trust fall and pray."**

You need help.  
You need `form-validate-av`.

---

## 🤔 Why the Name `form-validate-av`?

Well.  
Sometimes, names are born from moments of ✨inspiration✨.  
Other times… they’re born from character development.  
Let's just say **AV** taught me the real meaning of validation.  
Both in forms... and in life.  
(But we don't talk about that. 😌)

---

## What Even Is `form-validate-av`?

`form-validate-av` is a **lightweight, no-BS** form validation library for React that:

- Judges your form inputs harder than your aunt at family dinner 
- Fixes your errors faster than you fix your toxic texting habits 
- Reminds you (gently? no.) that "123" is NOT a secure password 

Basically, it’s the *best decision* you’ll make since you decided to stop texting them back. 😌

---

## ⚡ Installation (Because Obviously)

Install it like you install emotional damage:

```bash
npm install form-validate-av
```
or if you're ✨quirky✨:

```bash
yarn add form-validate-av
```

---

## 🛠 Usage: So Easy Even a Sleep-Deprived Developer Could Do It

```jsx
import React, { useState } from "react";
import { validateForm } from "form-validate-av";

const MyForm = () => {
  const [formData, setFormData] = useState({
    email: "",
    password: ""
  });
  const [errors, setErrors] = useState({});

  const rules = {
    email: { required: true, email: true },
    password: { required: true, minLength: 6 }
  };

  const handleChange = (e) => {
    setFormData({ ...formData, [e.target.name]: e.target.value });
  };

  const handleSubmit = (e) => {
    e.preventDefault();
    const validationErrors = validateForm(formData, rules);
    if (Object.keys(validationErrors).length === 0) {
      alert("Form submitted successfully 🎉✨");
    } else {
      setErrors(validationErrors);
    }
  };

  return (
    <form onSubmit={handleSubmit}>
      <input
        type="email"
        name="email"
        placeholder="Email"
        value={formData.email}
        onChange={handleChange}
      />
      {errors.email && <p>{errors.email}</p>}

      <input
        type="password"
        name="password"
        placeholder="Password"
        value={formData.password}
        onChange={handleChange}
      />
      {errors.password && <p>{errors.password}</p>}

      <button type="submit">Submit</button>
    </form>
  );
};

export default MyForm;
```

Literally that easy.  
Now your form actually *deserves* a Submit button.

---

## Features (aka Why You’ll Fall In Love Again)

- **Lightweight** — like your will to live during finals week
- **Fast** — because users have the attention span of a TikTok scroll
- **Customizable** — build your own rules, or break them, I’m not your mom
- **Emotionally Stable** — unlike *some* people (no shade… ok maybe a little)

---

## 📜 API: Your Little Black Book

| Rule         | Meaning                                    |
| ------------ | ------------------------------------------- |
| `required`   | *Don't ghost your fields.*                 |
| `email`      | *Pretend it's 2025 and you know what an email is.* |
| `minLength`  | *6 characters or you’re grounded.*         |
| `maxLength`  | *Boundaries exist for a reason, sweetie.*  |
| `pattern`    | *Because sometimes you gotta get fancy.*   |

---

## 👨‍💻 Made by

[Rishav Bhardwaz](https://github.com/rishav-bhardwaz) —  
Still fixing bugs and feelings at the same time.

---

# TL;DR
If your form fields are running wild like it’s 2007 and validation doesn’t exist,  
**`form-validate-av` is the hero you didn’t know you needed.**

---

# 🛋️ Bonus: Therapy Session with Your Forms

**Scene: A cozy virtual therapist’s office**  
*The forms sit on a couch, tissues in hand.*

**Email Field:**  
*"I just... I just want to be loved. I don't want people typing 'abc' and thinking it's okay..."*

**Password Field:**  
*"They keep entering 'password123'... I can't protect anyone with that!"*

**Form-Validate-AV (therapist, calmly sipping coffee):**  
*"Breathe. Set your boundaries. Demand respect. We'll add 'required' and 'minLength' rules together, one validation at a time."*

**Username Field (whispering):**  
*"Sometimes... they leave me blank. Like I don't even exist."*

**Form-Validate-AV:**  
*"You're valid. Literally. We'll set `required: true` and they'll never ignore you again."*

**[Session ends.]**  
The forms stand taller.  
The Submit button shines brighter.  
Validation has been achieved.  
**Growth. Healing. Closure.**

All thanks to `form-validate-av`. 

---