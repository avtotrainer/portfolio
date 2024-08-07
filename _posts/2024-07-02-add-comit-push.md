---
layout: post
title: ავტომატური განახლების სკრიპტი (add, commit, push) 
---

რეპოზიტორის გასაახლებლად მუდმივად გვიხდება სამი ბრძანების გამოყენება (add, commit, push). გონივრული იქნებოდა შესაბამისი სკრიპტის შექმნა


## ᲠᲝᲒᲝᲠ ᲨᲔᲕᲥᲛᲜᲐᲗ gIT-ᲘᲡ ᲡᲙᲠᲘᲞᲢᲘ ᲐᲕᲢᲝᲛᲐᲢᲘᲖᲐᲪᲘᲘᲡᲗᲕᲘᲡ

დღეს მინდა გაჩვენოთ, როგორ შეგიძლიათ შექმნათ მარტივი სკრიპტი, რომელიც ავტომატურად დაამატებს, დააკომიტებს და განაახლებს თქვენს ცვლილებებს Git-ში. ამ პოსტში ჩვენ შევქმნით სკრიპტს, რომელსაც დავარქმევთ `gitu`, კომიტის კომენტარი შესაძლებელი იქნება მიეთითოს პარამეტრის სახით ბრჭყალების გარეშე.

### ᲜᲐᲑᲘᲯᲘ 1: ᲡᲙᲠᲘᲞᲢᲘᲡ ᲨᲔᲥᲛᲜᲐ

პირველ რიგში, შექმენით ფაილი სახელად `gitu`. ამისთვის გამოიყენეთ შემდეგი ბრძანება ტერმინალში:

```bash
vim gitu
```

### ᲜᲐᲑᲘᲯᲘ 2: ᲡᲙᲠᲘᲞᲢᲘᲡ ᲓᲐᲬᲔᲠᲐ

გახსნილ ფაილში ჩაწერეთ შემდეგი სკრიპტი:

```bash
#!/bin/bash

# ვაყენებთ კომენტარს ნაგულისხმევად
DEFAULT_COMMENT=" კომენტარი არ მიეთითა"

# თუ გადაცემულია პარამეტრი, ვიყენებთ მას როგორც კომენტარს, სხვაგვარად ვიყენებთ ნაგულისხმევ კომენტარს
COMMENT=${@:-$DEFAULT_COMMENT}

# ვამატებთ ყველა ცვლილებას
git add .

# ვაკეთებთ კომიტს მითითებული კომენტარით
git commit -m "$COMMENT"

# ვპუშავთ ცვლილებებს რეპოზიტორიში
git push

# შეტყობინება წარმატებით შესრულების შესახებ
echo "ცვლილებები წარმატებით დამატებულია, კომიტირებულია და გაგზავნილია რეპოზიტორიში."
```

### ᲜᲐᲑᲘᲯᲘ 3: ᲡᲙᲠᲘᲞᲢᲘᲡ ᲨᲔᲡᲠᲣᲚᲔᲑᲐᲓᲝᲑᲐ

ფაილის შენახვის შემდეგ, სკრიპტი უნდა გავხადოთ შესრულებადი. ამისთვის გამოიყენეთ შემდეგი ბრძანება:

```bash
chmod +x gitu
```

### ᲜᲐᲑᲘᲯᲘ 4: ᲡᲙᲠᲘᲞᲢᲘᲡ ᲒᲐᲛᲝᲧᲔᲜᲔᲑᲐ

ახლა შეგიძლიათ გამოიყენოთ ეს სკრიპტი თქვენი Git რეპოზიტორიში. თუ გსურთ მიუთითოთ კომენტარი, შეგიძლიათ გააკეთოთ ეს შემდეგნაირად:

```bash
./gitu თქვენი კომენტარი
```

თუ კომენტარი არ მიუთითებთ, გამოყენებული იქნება ნაგულისხმევი კომენტარი "კომენტარი არ მიეთითა".

### დასკვნა

ამ მარტივი სკრიპტის საშუალებით, შეგიძლიათ სწრაფად და მარტივად დაამატოთ, დააკომიტოთ და განაახლოთ ცვლილებები Git-ში. ეს დაგეხმარებათ დაზოგოთ დრო და გაუმარტივოთ სამუშაო პროცესი. 

