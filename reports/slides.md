---
marp: true
theme: default
header: `pd.read_csv` is NOT all you need
footer: Adam Graham
---
<style>
section {
  background:rgb(251, 252, 225);
}
h1 {
    color: rgb(24, 68, 97);
    text-align: center;
}
h2 {
    color: rgb(45, 97, 24);
    text-align: center;
}
h3 {
    text-align: center;
}
</style>

<!-- paginate: skip -->

# `pd.read_csv` is NOT all you need:
## DataFrame validation in Python

Adam Graham, Data Scientist, ETA

---
<!-- paginate: true -->

## About Me (Adam)

- *Data Analyst/Scientist*, or maybe just *Data Tradie* (credit to **Kale Miller** for this term)
- Training in *Biostatistics*, Molecular Biology, Bioinformatics, `R`.
- I deal with *smol* data; from ~5 to 1e8 rows. Stuff that fits in RAM.
  - Once had to use a generator loop in python to parse something big.
- self-taught pythonista from:
  - Udemy
  - trying pandas before v0.20.0
  - these meetups
  - and using it in the real world

---

# Why validate anyway?

Real world data is messy and strange!

- Typos and ✨special characters✨
- 🪄 Excel magic behaviour.
- No one actually knows about [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) dates.
- Someone put a text comment in a numeric column.
- The monthly dataset arrives with different column names.

## The goal is to **avoid complexity in your code**

---

# Ad-hoc solutions to data validation

- Build your code against an ideal dataset
- Try it on some data and...
- ... find out someone used `Month-Day-Year`
- add a fix like this:
```python
data = pd.read_excel(filename)
data = do_some_stuff_to_it(data)
if check_day_month_order(data) is False:
    data = fix_the_datetime_mess(data)
do_more_stuff_to_the_data(data)
```

---

# Ad-hoc solutions to data validation

- This is not great! 🥲
- We introduce a lot of complexity in the middle of our scripts.
- Everything runs longer because it has to check stuff half-way through and you can't use elegant shortcuts.
- Eventually this becomes unmaintable as you try to cover the 1000 ways data can break your code.

---

# A better solution:
## Check your assumptions before you process your data!

1. Validate your data
2. Handle the invalid data
3. Finally; run your data through your pipeline
- This allows for *seperation of concerns*:
  - We can validate and munge our data in one place
  - analyse it in a different place
  - and write less code in the process!

---

## Jump to demo here?

### Yeah, why not? 🤷‍♀️

- Ad-hoc solutions
- Pandera
- Pola.rs
- ...
