---
layout: post
title: ᲕᲘᲠᲢᲣᲐᲚᲣᲠᲘ ᲒᲐᲠᲔᲛᲝ
description: ᲞᲠᲝᲒᲠᲐᲛᲘᲠᲔᲑᲐ ᲞᲘᲗᲝᲜᲖᲔ
---

პითონზე პროგრამირებისას, შეგიძლიათ კი არა, აუცილებლად უნდა დააყენოთ ვირტუალური გარემო, რომელიც სისტემაში შემოფარგლავს კონკრეტული პროექტის ინსტრუმენტებს და საშუალებას მოგცემთ აწარმოოთ რამოდენიმე პროექტის პროგრამირება. პროექტებისასთვის საჭირო ინსტრუმენტები შესაძლოა იყოს განსხვავებული და თქვენ არ დაგჭირდებათ ისინი დააყენოთ გლობალურად სისტემაში. ამასთან, სამომავლოდ ადვილია საჭირო ბიბლიოთეკების პაკეტის შედგენა, რადგან ვირტუალურ გარემოში მხოლოდ ის პაკეტები გექნებათ, რომელიც ამ პროექტის სამუშაოდაა საჭირო. Python 3-თვის ვირტუალური გარემოს დაყენება შეიძლება `venv` ინსტრუმენტის საშუალებით, რომელიც ჩაშენებულია Python-ის სტანტარტულ ბიბლიოთეკაში. აი, როგორ გავაკეთოთ ეს:

1. ვუშვებთ ტერმინალს, მე განვიხილავ მხოლოდ Linux/macOS გარემოს.

2. უნდა გადავიდეთ იმ კატალოგში, სადაც ვფიქრობთ ვირტუალური გარემოს შექმნას.

3. ვირტუალური გარემოს შესაქმნელი ბრძანება:

```
python3 -m venv myenv
```

აქ  `myenv` - ეს არის თქვენი ვირტუალური გარემოს სახელი. თქვენ შეგიძლიათ აირჩიოთ ნებისმიერი სხვა. მე ამ კატალოგს ყოველთვის ვარქმევ იგივე სახელს - `venv`.

4. ამ ბრძანებით თქვენს ამორჩეულ კატალოგში შეიქმნება ვირტუალური გარემო.

5. შექმნილ გარემოს სჭირდება გააქტიურება, ამისათვის საჭიროა ბრძანება:

   - Windows-ში:

     ```
     myenv\Scripts\activate
     ```

   - macOS და Linux-ში:

     ```
     source myenv/bin/activate
     ```

6. აქტივაციის შემდეგ თქვენმა ტერმინალმა უნდა გიჩვენოთ, რომ თქვენ იმყოფებით ვირტუალურ გარემოში. ეს ჩვენება დამოკიდებულია იმაზეც, თქვენ რანაირად გაქვთ დაწყობილი ტერმინალი. ამის შემდეგ შეგიძლიათ დააყენოთ თქვენი პროექტისათვის საჭირო პაკეტები და იმუშაოთ ამ იზოლირებულ გარემოში Python-ის გლობალურ გარემოზე ან გარემოს გავლენის გარეშე.

სამუშაოს დასასრულს შეგიძლიათ ვირტუალური გარემოს დეაქტივაცია, ამისათვის ტერმინალში არის ბრძანება `deactivate`, რათა გამოხვიდეთ იქიდან.
