summary mastering git

resources :
    -https://learngitbranching.js.org/



1. Rebase -> get copy of commit from a branch to another branch -> copy a snapshot
    command : git rebase branch_name

2. Merge -> combine all some work from branch to another -> combine a work/result

3. Detached Head -> mengganti head ke salah satu commit hash yang ada. dengan kata lain, biasanya HEAD menunjunk sebuah branch,
    Detaching head menunjuk salah satu commit hash untuk di jadikan referensi HEAD.
    - HATI-HATI ketika menggunakan ini, jika di commit ke sini, perubahan tidak akan menunjuk ke salah satu branch, dan log akan hilang
4. Submodules
    referensi : https://www.git-tower.com/learn/git/ebook/en/command-line/advanced-topics/submodules#start

    penjelasan :
        - dalam project, libraries dan third party biasa kita ikutkan dalam project kita dan kita commit bersama main project kita.
        - hal itu sebenarnya di terima, tetapi bukan hal yang bagus, karena bercampur antara library dengan commit code perubahan kita
        - solusinya adalah submodules
        - submodules menjadi solusi untuk menambahkan part tambahan yang 'secara tidak langsung" berhubungan dengan project kita
        - submodules berarti memisahkan beberapa part untuk kedalam satu bagian yang didalamnya bisa kita lakukan hal yang sama dengan main project kita.
    
    bagaimana clone project with submodules
        ada 2 opsi 
        1. add "--recurse-submodules" pada saat melakukan git clone
        2. jika melakukan clone biasa, setelah itu bisa melakukan command "git submodule update --init --recursive"




advanced -> 
    -> git checkout HEAD~^2~2
    -> git branch branch_name~^2~2 -> buat branch dan menunjuk ke hash ke atas posisi ke-2