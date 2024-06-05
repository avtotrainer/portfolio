---
layout: post
title: PIP-ᲘᲡ ᲒᲐნᲐᲮᲚᲔᲑᲐ
description: ᲞᲘᲗᲝᲜᲘᲡ ᲞᲐᲙᲔᲢᲔᲑᲘᲡ ᲛᲔᲜᲔᲯᲔᲠᲘ
---

თქვენი პროექტის პრიტუალერი გარემოს შიგნით მიზანშეწონილია განახლებული იყოს pip პაკეტების მენეჯერი, ამისათვის პირველ რიგში უნდა გააქტიურდეს ვირტუალური გარემო, ხოლო შემდეგ უნდა შეასურლოთ pip მენეჯერის განახლების ბრძანება.

აი როგორ ხდება ეს:

1. გააქტიურეთ თქვენი ვირტუალური გარემო:

   - Windows-ისთვის:
     ```
     myenv\Scripts\activate
     ```

   - macOS და Linux-თვის:
     ```
     source myenv/bin/activate
     ```

2. ვირუტუალური გარემოს გააქტიურების შემდეგ შეასრულეთ ბრძანება pip მენეჯერის გასაახლებლად:

   ```
   python -m pip install --upgrade pip
   ```

   აქ `python` - ეს არის ვირტუალურ გარემოში Python-ის გასაშვები ბრძანება. არაა საჭირო `python3` ბრძანების გამოყენება იმიტომ, რომ თქვენ იმყოფებით ვირტუალური გარემოს შიგნით, სადაც ისედაც გაქვთ ერთადერთი Python 3.

3. ამ ბრძანების შესრულების შემდეგ pip მენეჯერის განახლება მოხდება ბოლო ვერსიამდე.