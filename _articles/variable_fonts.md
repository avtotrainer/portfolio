---
layout: post
title: ᲪᲕᲐᲚᲔᲑᲐᲓᲘ ᲨᲠᲘᲤᲢᲔᲑᲘ
description: ვარიაციები ერთი და იგივე შრიფტიდან
---

[მეზობელ სტატიაში](https://pf.din.ge/articles/google-fonts/) დავწერე Google-ის კოლექციაში არსებულ ორად ორ ქართულ შრიფტზე. Google fonts არის სისტემა, რომელიც შრიფტის ერთი სახელის ქვეშ შრიფტების მთელ კოლექციას იყენებს. ასე დიზაინერს აძლევს საშუალებას გამიოყენოს რამოდენიმე დამატებითი თვისება, ერთერთი ესაა შრიფტის წონა:

<div class="noto-sans-georgian-w100"> არხოტის ცასავით ლურჯი გაქვს თვალები font-weight: 100; </div>
<div class="noto-sans-georgian-w200"> არხოტის ცასავით ლურჯი გაქვს თვალები font-weight: 200; </div>
<div class="noto-sans-georgian-w300"> არხოტის ცასავით ლურჯი გაქვს თვალები font-weight: 300; </div>
<div class="noto-sans-georgian-w400"> არხოტის ცასავით ლურჯი გაქვს თვალები font-weight: 400; </div>
<div class="noto-sans-georgian-w500"> არხოტის ცასავით ლურჯი გაქვს თვალები font-weight: 500; </div>
<div class="noto-sans-georgian-w600"> არხოტის ცასავით ლურჯი გაქვს თვალები font-weight: 600; </div>
<div class="noto-sans-georgian-w700"> არხოტის ცასავით ლურჯი გაქვს თვალები font-weight: 700; </div>
<div class="noto-sans-georgian-w800"> არხოტის ცასავით ლურჯი გაქვს თვალები font-weight: 800; </div>
<div class="noto-sans-georgian-w900"> არხოტის ცასავით ლურჯი გაქვს თვალები font-weight: 900; </div>
<div class="noto-serif-georgian-w900"> არხოტის ცასავით ლურჯი გაქვს თვალები font-weight: 900; </div>
<div class="noto-serif-georgian-w800"> არხოტის ცასავით ლურჯი გაქვს თვალები font-weight: 800; </div>
<div class="noto-serif-georgian-w700"> არხოტის ცასავით ლურჯი გაქვს თვალები font-weight: 700; </div>
<div class="noto-serif-georgian-w600"> არხოტის ცასავით ლურჯი გაქვს თვალები font-weight: 600; </div>
<div class="noto-serif-georgian-w500"> არხოტის ცასავით ლურჯი გაქვს თვალები font-weight: 500; </div>
<div class="noto-serif-georgian-w400"> არხოტის ცასავით ლურჯი გაქვს თვალები font-weight: 400; </div>
<div class="noto-serif-georgian-w300"> არხოტის ცასავით ლურჯი გაქვს თვალები font-weight: 300; </div>
<div class="noto-serif-georgian-w200"> არხოტის ცასავით ლურჯი გაქვს თვალები font-weight: 200; </div>
<div class="noto-serif-georgian-w100"> არხოტის ცასავით ლურჯი გაქვს თვალები font-weight: 100; </div>

ამ მაგალითში მოყვანილია ხსენებული ქართული შრიფტები (Noto Sans Georgian და Noto Serif Georgian).

შრიფტების სიმძიმე, რომელის ვიზუალური გარჩევაა შესაძლებელი, დიფერენცირებულია ასე:

  - Thin 100
  - ExtraLight 200
  - Light 300
  - Regular 400
  - Medium 500
  - SemiBold 600
  - Bold 700
  - ExtraBold 800
  - Black 900

  ამ მნიშვნელობების გარდა შესაძლებელია ნებისმიერი რიცხვის გამოყენება 100-900 დიაპაზონიდან, მაგალითად თუ დავწერთ font-weight: 733; ასოები მას დაემორჩილებიან.

 მეორე პარამეტრია **font-variation-settings**, რომელიც იცვლება 62.5-100 დიაპაზონში. ცვლადების სახით ის წარმოდგენილია შემდეი ბიჯით:

   - ExtraCondensed 62.5
   - Condensed 75
   - SemiCondensed 87.5
   - Normal 100

 ნახეთ ტექსტები შესადარებლად Regular სიმძიმის შრიფტების მაგალითზე:

<div class="noto-sans-georgian-v62"> არხოტის ცასავით ლურჯი გაქვს თვალები 62.5; </div>
<div class="noto-sans-georgian-v75"> არხოტის ცასავით ლურჯი გაქვს თვალები 75 </div>
<div class="noto-sans-georgian-v87"> არხოტის ცასავით ლურჯი გაქვს თვალები 87.5 </div>
<div class="noto-sans-georgian-v100"> არხოტის ცასავით ლურჯი გაქვს თვალები 100 </div>
<div class="noto-serif-georgian-v100"> არხოტის ცასავით ლურჯი გაქვს თვალები 100 </div>
<div class="noto-serif-georgian-v87"> არხოტის ცასავით ლურჯი გაქვს თვალები 87.5 </div>
<div class="noto-serif-georgian-v75"> არხოტის ცასავით ლურჯი გაქვს თვალები 75 </div>
<div class="noto-serif-georgian-v62.5"> არხოტის ცასავით ლურჯი გაქვს თვალები 62.5 </div>

ყველა ბიჯს შორის განსხვავება არის თანაბრად 12.5, ეს ნახტომები თვალში შესამჩნევ ცვლილებებს იწვევს, თუმცა შესაძლებელია დიაპაზონიდან ნებისმიერი მნიშვნელობის გამოყენება.

Google Fonts-ის შრიფტების შესაფასებლად დავაკვირდეთ შემდეგ ტექსტებს სხვადასხვა ენაზე (სხვადასხვა UTF-8 დიაპაზონი).

<div class="h1-serif">ᲚᲝᲠᲔᲜ ᲘᲑᲡᲣᲛ ᲓᲝᲚᲝᲠ ᲐᲛᲔᲢ</div>

<div class="h1-serif">LOREN IBSUM DOLOR AMET</div>

<div class="h1-serif">ЛОРЕН ИПСУМ ДОЛОР АМЕТ</div>

ამ ტექსტების სტილი იდენტურია და მათი შრიფტის ოჯახი არის `Noto Serif Georgian`

ხოლო შემდეგი სამი ხაზის კი `Noto Sans Georgian`:


<div class="h1-sans">ᲚᲝᲠᲔᲜ ᲘᲑᲡᲣᲛ ᲓᲝᲚᲝᲠ ᲐᲛᲔᲢ</div>

<div class="h1-sans">LOREN IBSUM DOLOR AMET</div>

<div class="h1-sans">ЛОРЕН ИПСУМ ДОЛОР АМЕТ</div>

ენების განსხვავების მიუხედავად ტექსტების სტილის მსგავსება უდაოა. ქართული ტექსტებიან კონტენტში ყოველთვის ასე არ არის. ქართული Web შრიფტებით მყისიერად ასეთი ეშედეგის მიღება არაა ადვილი. როგორ აკეთებს ამას Google, შეიძლება ნახოთ css ფაილში, [ბმულზე](https://fonts.googleapis.com/css2?family=Noto+Sans+Georgian:wdth,wght@62.5..100,100..900&family=Noto+Serif+Georgian:wght@100..900&display=swap). ყველა განსხვავებული შემთხვევისათვის Google იყენებს სხვადასხვა შრიფტებს, ხოლო რომელი შრიფტი უნდა იქნას გამოყენებული, ამას წყვეტს ბრაუზერი კონტენტიდან გამოდინარე.

ვფიქრობ, რომ ამ საიტზე, სადაც ასევე შერეულია ენები, Google-ის შრიფტების ამორჩევა იყო სწორი გადაწყვეტილება.


