# Majās darbs 2.
## Uzdevumi atbildes
13. Salīdzināt failu hash no mapes module_1 un module_2.

``
git hash-object git_repos/module_1/assets/pic1.jpg
31449f04d1e6119bde1f9974a5134677fee31b5b
``
``
git hash-object git_repos/module_2/assets/pic1.jpg
31449f04d1e6119bde1f9974a5134677fee31b5b
``

16. Pārbaudīt kādas izmaiņas tika veiktas iepriekšējās nedēļas laikā. Atrast vismaz divus veidus kā to izdarīt.
``
git log --since=2.weeks
git log --until 11.04.2022
``
17. Atrast commit kurus veica autors - “Laura Pacilio” 
``
git log --author=="Laura Pacilio"
``
18. Atrast vai Laura ir veikusi commit pagājušā gada septembrī?
Jā, to varam redzet ar komandu:
``
git log --author="Laura Pacilio" --pretty --since="2021-09-01"
``
Pedejaīs commit bija 20.04

commit e68ad5ec463fbfa2a9c19abc54f60efb4b779141 (origin/update-TF-WORKSPACE-variable)
Author: Laura Pacilio <83350965+laurapacilio@users.noreply.github.com>
Date:   Wed Apr 20 18:57:50 2022 -0400

Pirmais no pāgajušā gada septembri bija 02.09.2021

commit 73a3bb27029054a0c14f2aef8081900bf821c809
Merge: 05f21cdff b8a0929a5
Author: Laura Pacilio <83350965+laurapacilio@users.noreply.github.com>
Date:   Thu Sep 2 14:47:38 2021 -0400

19. Vai Laura ir veikusi commit vakar?
- Ne, pēdējais commits bija 20.04.2022

commit e68ad5ec463fbfa2a9c19abc54f60efb4b779141 (origin/update-TF-WORKSPACE-variable)
Author: Laura Pacilio <83350965+laurapacilio@users.noreply.github.com>
Date:   Wed Apr 20 18:57:50 2022 -0400

20. Atlasot rezultātus no pagājušā gada 20 līdz 21 aprīlim var atrast commit kurš ir datēts ar 16 aprīli? Kāpēc tā ir? Atbildi apkopot module_2 > README.md un
pārsūtīt rezultātu Github.

Parasta git log komanda rada lokalo "Author" commit datu, tomer mēs varam redzet commit f8493bf5cd78bc2a723f5ddc6f6bceb0e08813ea tapec ka viņš bija nosutits uz repozitoriju 20.04.2021, to mes varam redzet ja pievienot pie git log  —pretty=fuller parametru. 
`` 
git log —pretty=fuller f8493bf5cd78bc2a723f5ddc6f6bceb0e08813ea
Author:     James Bardin <j.bardin@gmail.com>
AuthorDate: Fri Apr 16 17:11:27 2021 -0400
Commit:     James Bardin <j.bardin@gmail.com>
CommitDate: Tue Apr 20 17:04:56 2021 -0400
