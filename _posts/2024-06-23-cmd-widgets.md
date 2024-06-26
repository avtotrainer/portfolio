---
layout: post
title: ბრძანების ვიჯეტები 
---

ტერმინალის ბრძანების ხაზში შესაძლებელია სხვადასხვა ვიჯეტის გამოყენება

## ბრძანების ხაზის ვიჯეტები ტერმინალში

zsh საშუალებას იძლევა ბრძანების ხაზთან ვიმუშაოთ უფრო მეტი კომფორტით. რაიმე მოქმედება წარმოდგენილია ვიჯეტების სახით, რომლებსაც გააჩნიათ შესაბამისი კლავიშების კომბინაცია. მოვიყვან მათი პრაქტიკული გამოყენების ამგალითებს

### ნავიგაციის და რედაქტირების ძირითადი ბრძანებები

- `^@` (Ctrl + @): `set-mark-command` - დასვამს ჭდეს კურსორის მიმდინარე პოზიციაში.
- `^A` (Ctrl + A): `beginning-of-line` - გადაიყვანს კურსორს სტრიქონის დასაწყისში.
- `^B` (Ctrl + B): `backward-char` - გადაიყვანს კურსორს ერთი სიმბოლოთი უკან.
- `^D` (Ctrl + D): `delete-char-or-list` - წაშლის სიმბოლოს კურსორის ქვეშ ან გამოიტანს შესაძლო ვარიანტების სიას.
- `^E` (Ctrl + E): `end-of-line` - კურსორს გაიყვანს სტრიქონის ბოლოში.
- `^F` (Ctrl + F): `forward-char` - კურსორს გადაიყვავს ერთი სიმბოლოთი წინ.
- `^G` (Ctrl + G): `send-break` - გააგზავნის წყვეტის სიგნალს.
- `^H` (Ctrl + H): `backward-delete-char` - წაშლის კურსრის წინა სიმბოლოს (Backspace-ს ანალოგი).
- `^I` (Ctrl + I): `expand-or-complete` - გააფართოებს მიმდინარე ბრძანებას ან გააკეთებს ავტოდამატებას (Tab-ის ანალოგი).
- `^J` (Ctrl + J): `accept-line` - მიმდინარე სტრიქონის დამოწმება(Enter-ის ანალოგი).
- `^K` (Ctrl + K): `kill-line` - წაშლის ტექსტს კურსორიდან სტრიქონის ბოლომდე.
- `^L` (Ctrl + L): `clear-screen` - გაასუფთავებს ეკრანს.
- `^M` (Ctrl + M): `accept-line` - მიმდინარე სტრიქონის დამოწმება(Enter-ის ანალოგი).
- `^N` (Ctrl + N): `down-line-or-history` - გადაიტანს კურსორს სტრიქონით დაბლა ან ქვემოთ ისტორიაში.
- `^O` (Ctrl + O): `accept-line-and-down-history` - მიმდინარე სტრიქონის დამოწმება და გადააგილება ისტორიაში ქვემოთ.
- `^P` (Ctrl + P): `up-line-or-history` - კურსორის გადატანა სტრიქონით მაღლა ან მაღლა ისტორიაში.
- `^Q` (Ctrl + Q): `push-line` - ინახავს მიმდინარე სტრიქონს და ასუფთავებს ხაზს.
- `^R` (Ctrl + R): `history-incremental-search-backward` - ბრძანებების ისტორიაში ეძებს უკან.
- `^S` (Ctrl + S): `history-incremental-search-forward` - ბრძანებების ისტორიაში ეძებს წინ.
- `^T` (Ctrl + T): `transpose-chars` - კურსორის წინ ორ სიმბოლოს გაუცვლის ადგილებს.
- `^U` (Ctrl + U): `kill-whole-line` - წაშლის მთლიან სტრიქონს.
- `^V` (Ctrl + V): `quoted-insert` - Вставляет следующий введенный символ буквально.
- `^W` (Ctrl + W): `backward-kill-word` - წაშლის კურსორის წინა სიტყვას.
- `^X^B` (Ctrl + X, შემდეგ B): `vi-match-bracket` - გადაადგილებს კურსორს შესაბამის ფრჩხილამდე (vi რეჟიმი).
- `^X^E` (Ctrl + X, შემდეგ E): `edit-command-line` - მიმდინარე ბრძანებას დაარედაქტირებს გარე რედაქტორში.
- `^X^F` (Ctrl + X, შემდეგ F): `vi-find-next-char` - მოძებნის შემდეგ სიმბოლოს (vi რეჟიმი).
- `^X^J` (Ctrl + X, შემდეგ J): `vi-join` - მიმდინარე სტრიქონს გააერთიანებს მომდევნოსთან (vi რეჟიმი).
- `^X^K` (Ctrl + X, შემდეგ K): `kill-buffer` - წაშლის ბუფერის შემადგენლობას.
- `^X^N` (Ctrl + X, შემდეგ N): `infer-next-history` - კარნახობს შემდეგ ბრძანებას ისტორიიდან.
- `^X^O` (Ctrl + X, შემდეგ O): `overwrite-mode` - ჩართავს ტექსტის ზედ გადაწერის რეჟიმს.
- `^X^R` (Ctrl + X, შემდეგ R): `_read_comp` - შეასრულებს წაკითხვას და ავტოდამატებას.
- `^X^U` (Ctrl + X, შემდეგ U): `undo` - გააუქმებს ბოლო ბრძანებას.
- `^X^V` (Ctrl + X, შემდეგ V): `vi-cmd-mode` - ჩართავს ბრძანებების vi რეჟიმს.
- `^X^X` (Ctrl + X, შემდეგ X): `exchange-point-and-mark` - გადაცვლის მიმდინარე პოზიციას და ჭდეს.
- `^X*` (Ctrl + X, შემდეგ *): `expand-word` - აფართოებს მიმდინარე სიტყვას.
- `^X=` (Ctrl + X, შემდეგ =): `what-cursor-position` - აჩვენებს კურსორის მიმდინარე პოზიციას.
- `^X?` (Ctrl + X, შემდეგ ?): `_complete_debug` - ჩართავს ავტოდამატების დებაგს.
- `^XC` (Ctrl + X, შემდეგ C): `_correct_filename` - აკორექტირებს ფაილის სახელს.
- `^XG` (Ctrl + X, შემდეგ G): `list-expand` - აფართოებს და გამოაქვს შესაძლო დამატებების სიას.
- `^Xa` (Ctrl + X, შემდეგ a): `_expand_alias` - აფართოებს ალიასს.
- `^Xc` (Ctrl + X, შემდეგ c): `_correct_word` - აკორექტირებს სიტყვას.
- `^Xd` (Ctrl + X, შემდეგ d): `_list_expansions` - გამოაქვს გაფართოებების სია.
- `^Xe` (Ctrl + X, შემდეგ e): `_expand_word` - აფართოებს სიტყვას.
- `^Xg` (Ctrl + X, შემდეგ g): `list-expand` - აფართოებს და გამოაქვს სია შესძლო დამატებებისა.
- `^Xh` (Ctrl + X, შემდეგ h): `_complete_help` - აჩვენებს განმარტებას ავტოდამატებისათვის.
- `^Xm` (Ctrl + X, შემდეგ m): `_most_recent_file` - პოულობს ბოლო შეცვლილ ფაილს.
- `^Xn` (Ctrl + X, შემდეგ n): `_next_tags` - პოულობს შემდეგ ტეგს.
- `^Xr` (Ctrl + X, შემდეგ r): `history-incremental-search-backward` - ბრძანებების ისტორიაში ეძებს უკან.
- `^Xs` (Ctrl + X, შემდეგ s): `history-incremental-search-forward` - ეძებს წინ ბრძანებების ისტორიაში.
- `^Xt` (Ctrl + X, შემდეგ t): `_complete_tag` - შეავსებს ტეგს.
- `^Xu` (Ctrl + X, შემდეგ u): `undo` - გააუქმებს ბოლო მოქმედებას.
- `^X~` (Ctrl + X, შემდეგ ~): `_bash_list-choices` - ვარიანტების სიის გამოტანა (Bash-ის ანალოგი).
- `^Y` (Ctrl + Y): `yank` - ჩასვამს ბოლო მოჭრილ ტექსტს.
- `^[^D` (Esc, შემდეგ Ctrl + D): `list-choices` - გამოიტანს შესაძლო დამატებების სიას.
- `^[^G` (Esc, შემდეგ Ctrl + G): `send-break` - აგზავნის წვეტის სიგნალს.
- `^[^H` (Esc, შემდეგ Ctrl + H): `backward-kill-word` - კურსორის წინა სიტყვის წაშლა.
- `^[^I` (Esc, შემდეგ Ctrl + I): `self-insert-unmeta` - სიმბოლოს ჩასმა.
- `^[^J` (Esc, შემდეგ Ctrl + J): `self-insert-unmeta` - სიმბოლოს ჩასმა.
- `^[^L` (Esc, შემდეგ Ctrl + L): `clear-screen` - ეკრანის გასუფთავება.
- `^[^M` (Esc, შემდეგ Ctrl + M): `self-insert-unmeta` - სიმბოლოს ჩასმა.
- `^[^_` (Esc, შემდეგ Ctrl + _): `copy-prev-word` - აკოპირებს წინა სიტყვას.
- `^[ ` (Esc, შემდეგ пробел): `expand-history` - ბრძანებების ისტორიის გაფართოება.
- `^[!` (Esc, შემდეგ !): `expand-history` - ბრძანებების ისტორიის გაფართოება.
- `^[\"` (Esc, შემდეგ "): `quote-region` - რეგიონის ციტირება.
- `^[$` (Esc, შემდეგ $): `spell-word` - სიტყვის ორთოგრაფიული შემოწმება.
- `^['` (Esc, შემდეგ '): `quote-line` - სტრიქონის ციტირება.
- `^[,` (Esc, შემდეგ ,): `_history-complete-newer` - ამთავრებს უფრო ახალ ბრძანებას ისტორიიდან.
- `^[-` (Esc, შემდეგ -): `neg-argument` - შეყავს უარყოფითი არგუმენტი.
- `^[.` (Esc,  .): `insert-last-word` - ჩასვამს ბოლო სიტყვას.
- `^[\/` (Esc, შემდეგ /): `_history-complete-older` - დაამთავრებს ისტორიაში უფრო ძველ ბრძანებას.
- `^[0` (Esc, შემდეგ 0): `digit-argument` - Вводит цифровой аргумент.
- `^[1` (Esc, შემდეგ 1): `digit-argument` - შეყავს ციფრული არგუმენტი.
- `
