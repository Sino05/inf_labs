# Отчет по лабораторной работе № 1
## по курсу "Фундаментальная информатика"

Студент группы <M8O-108Б-23> Sheraliev Sino 

Работа выполнена 

Преподаватель: каф. 806 Севастьянов Виктор Сергеевич

1. **Тема**: Название темы изучение github
2. **Цель работы**: научится ползоватся github
3. **Задание (вариант №<номер варианта если есть>)**: #1
4. **Идея, метод, алгоритм решения задачи**: 1. Завести репозиторий на Github
2.Создать отдельную папку в репозитории под данную лабораторную работу
3.В папке создать файл отчета в формате Markdown,
4.Создать отдельную ветку в репозитории для выполнения задания
5.В ветке создать коммит, включающий в себя листинг выполненных действий в терминале и отчет в Markdown
Смержить созданную ветку в ветку main
5. **Сценарий выполнения работы**: 1 зарегистрировался на github,2 завел репозиторию,3  начал выполнять задание, 4 закончил.

6. **Протокол**: 
```bash
sinosheraliev@MacBook-Air-Dilshod laba % git init
Initialized empty Git repository in /Users/sinosheraliev/Desktop/laba/.git/
sinosheraliev@MacBook-Air-Dilshod laba % mkdir 1 
sinosheraliev@MacBook-Air-Dilshod laba % la
zsh: command not found: la
sinosheraliev@MacBook-Air-Dilshod laba % ls
1
sinosheraliev@MacBook-Air-Dilshod laba % touch 1/report.md
sinosheraliev@MacBook-Air-Dilshod laba % git remote add origin https://github.com/Sino05/labs.git
git branch -M main
git push -u origin main
error: src refspec main does not match any
error: failed to push some refs to 'https://github.com/Sino05/labs.git'
sinosheraliev@MacBook-Air-Dilshod laba % git add ,
fatal: pathspec ',' did not match any files
sinosheraliev@MacBook-Air-Dilshod laba % git add .
sinosheraliev@MacBook-Air-Dilshod laba % git commit -m "init"
[main (root-commit) 539ed09] init
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 1/report.md
sinosheraliev@MacBook-Air-Dilshod laba % git remote add origin https://github.com/Sino05/labs.git
git branch -M main
git push -u origin main
         sinosheraliev@MacBook-Air-Dilshod laba % git remote -v
origin	https://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@github.com/Sino05/labs (fetch)
origin	https://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@github.com/Sino05/labs (push)
sinosheraliev@MacBook-Air-Dilshod laba % ls -la.ssh/
ls: invalid option -- .
usage: ls [-@ABCFGHILOPRSTUWabcdefghiklmnopqrstuvwxy1%,] [--color=when] [-D format] [file ...]
sinosheraliev@MacBook-Air-Dilshod laba % git confing --global user.email sino.sheraliev05@gmail.com
git: 'confing' is not a git command. See 'git --help'.

The most similar command is
	config
sinosheraliev@MacBook-Air-Dilshod laba % git confing --list
git: 'confing' is not a git command. See 'git --help'.

The most similar command is
	config
sinosheraliev@MacBook-Air-Dilshod laba % git config --global user.name "Sino05"
sinosheraliev@MacBook-Air-Dilshod laba % git config --global user.email sino.sheraliev05@gmail.com
sinosheraliev@MacBook-Air-Dilshod laba % git config --list
credential.helper=osxkeychain
init.defaultbranch=main
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
user.name=Sino05
user.email=sino.sheraliev05@gmail.com
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
core.ignorecase=true
core.precomposeunicode=true
remote.origin.url=https://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@github.com/Sino05/labs
remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*
branch.main.remote=origin
branch.main.merge=refs/heads/main
sinosheraliev@MacBook-Air-Dilshod laba % cd ~
sinosheraliev@MacBook-Air-Dilshod ~ % ls -la .ssh/
ls: .ssh/: No such file or directory
sinosheraliev@MacBook-Air-Dilshod ~ % ssh-keygen -t ed25519 -C "sino.sheraliev05@gmail.com"
Generating public/private ed25519 key pair.
Enter file in which to save the key (/Users/sinosheraliev/.ssh/id_ed25519): 
Created directory '/Users/sinosheraliev/.ssh'.
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /Users/sinosheraliev/.ssh/id_ed25519
Your public key has been saved in /Users/sinosheraliev/.ssh/id_ed25519.pub
The key fingerprint is:
SHA256:T3/XfrGY+DQoxvlwaewEpLyYKzb1qzn2PC79ye95rQU sino.sheraliev05@gmail.com
The key's randomart image is:
+--[ED25519 256]--+
|                 |
|                 |
|         .       |
|      . o        |
|       oS..  E   |
|     .o oo+.o ...|
|    .oo. *.Boo=.=|
|   + +++o X.o=o=.|
|  . ++*=++o*oo. o|
+----[SHA256]-----+
sinosheraliev@MacBook-Air-Dilshod ~ % ls -a ~/.ssh
.		..		id_ed25519	id_ed25519.pub
sinosheraliev@MacBook-Air-Dilshod ~ % pbcopy < ~/.ssh/id_ed25519.pub
sinosheraliev@MacBook-Air-Dilshod ~ % ssh -T git@github.com
The authenticity of host 'github.com (140.82.121.4)' can't be established.
ED25519 key fingerprint is SHA256:+DiY3wvvV6TuJJhbpZisF/zLDA0zPMSvHdkr4UvCOqU.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'github.com' (ED25519) to the list of known hosts.
Hi Sino05! You've successfully authenticated, but GitHub does not provide shell access.
sinosheraliev@MacBook-Air-Dilshod ~ % cd ~/laba
cd: no such file or directory: /Users/sinosheraliev/laba
sinosheraliev@MacBook-Air-Dilshod ~ % ls
Applications	Desktop		Documents	Downloads	Library		Movies		Music		Pictures	Public		PycharmProjects	programm.py	take
sinosheraliev@MacBook-Air-Dilshod ~ % cd ~
sinosheraliev@MacBook-Air-Dilshod ~ % pwd
/Users/sinosheraliev
sinosheraliev@MacBook-Air-Dilshod ~ % cd Users
cd: no such file or directory: Users
sinosheraliev@MacBook-Air-Dilshod ~ % cd User
cd: no such file or directory: User
sinosheraliev@MacBook-Air-Dilshod ~ % cd Desktop 
sinosheraliev@MacBook-Air-Dilshod Desktop % ls
Certificate Student.docx				laba							Снимок экрана 2023-10-06 в 23.19.14.png
Kurumi							main 2.py						Снимок экрана 2023-10-06 в 23.19.16.png
Python							main 3.py						Снимок экрана 2023-10-06 в 23.19.18.png
Report-template.md№1					main.py							Снимок экрана 2023-10-06 в 23.19.23.png
Scratch 3						music							Снимок экрана 2023-10-07 в 21.51.14.png
Visual Studio Code					skrin							Снимок экрана 2023-10-07 в 22.28.58.png
character						type							Снимок экрана 2023-10-07 в 22.37.19.png
class work						vsc							геометрия.docx
home work						Снимок экрана 2023-09-27 в 22.19.44.png
sinosheraliev@MacBook-Air-Dilshod Desktop % cd laba
sinosheraliev@MacBook-Air-Dilshod laba % ls
1
sinosheraliev@MacBook-Air-Dilshod laba % mkdir 2 3 4 5 6 7 8 9 10
sinosheraliev@MacBook-Air-Dilshod laba % ls
1	10	2	3	4	5	6	7	8	9
sinosheraliev@MacBook-Air-Dilshod laba % cd 1
sinosheraliev@MacBook-Air-Dilshod 1 % ls
report		report.md
sinosheraliev@MacBook-Air-Dilshod 1 % cd ..
sinosheraliev@MacBook-Air-Dilshod laba % git remote add origin git@github.com:Sino05/labs.git
error: remote origin already exists.
sinosheraliev@MacBook-Air-Dilshod laba % git remote -v
origin	https://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@github.com/Sino05/labs (fetch)
origin	https://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@github.com/Sino05/labs (push)
sinosheraliev@MacBook-Air-Dilshod laba % git remote add origin git@github.com:Sino05/LABA.git
error: remote origin already exists.
sinosheraliev@MacBook-Air-Dilshod laba % git remote add orig git@github.com:Sino05/LABA.git
sinosheraliev@MacBook-Air-Dilshod laba % git remote -V
error: unknown switch `V'
usage: git remote [-v | --verbose]
   or: git remote add [-t <branch>] [-m <master>] [-f] [--tags | --no-tags] [--mirror=<fetch|push>] <name> <url>
   or: git remote rename [--[no-]progress] <old> <new>
   or: git remote remove <name>
   or: git remote set-head <name> (-a | --auto | -d | --delete | <branch>)
   or: git remote [-v | --verbose] show [-n] <name>
   or: git remote prune [-n | --dry-run] <name>
   or: git remote [-v | --verbose] update [-p | --prune] [(<group> | <remote>)...]
   or: git remote set-branches [--add] <name> <branch>...
   or: git remote get-url [--push] [--all] <name>
   or: git remote set-url [--push] <name> <newurl> [<oldurl>]
   or: git remote set-url --add <name> <newurl>
   or: git remote set-url --delete <name> <url>

    -v, --verbose         be verbose; must be placed before a subcommand

sinosheraliev@MacBook-Air-Dilshod laba % git remote -v
orig	git@github.com:Sino05/LABA.git (fetch)
orig	git@github.com:Sino05/LABA.git (push)
origin	https://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@github.com/Sino05/labs (fetch)
origin	https://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@github.com/Sino05/labs (push)
sinosheraliev@MacBook-Air-Dilshod laba % git remote -v
orig	git@github.com:Sino05/LABA.git (fetch)
orig	git@github.com:Sino05/LABA.git (push)
origin	https://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@github.com/Sino05/labs (fetch)
origin	https://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@github.com/Sino05/labs (push)
sinosheraliev@MacBook-Air-Dilshod laba % git add --all
sinosheraliev@MacBook-Air-Dilshod laba % git commit -m 'error'
[main 049174e] error
 2 files changed, 60 insertions(+)
 create mode 100644 .DS_Store
 create mode 100644 1/report
sinosheraliev@MacBook-Air-Dilshod laba % git push -u orig master
error: src refspec master does not match any
error: failed to push some refs to 'github.com:Sino05/LABA.git'
sinosheraliev@MacBook-Air-Dilshod laba % git push -u orig main
To github.com:Sino05/LABA.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'github.com:Sino05/LABA.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
sinosheraliev@MacBook-Air-Dilshod laba % git init 
Reinitialized existing Git repository in /Users/sinosheraliev/Desktop/laba/.git/
sinosheraliev@MacBook-Air-Dilshod laba % git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
sinosheraliev@MacBook-Air-Dilshod laba % git push
remote: Repository not found.
fatal: repository 'https://github.com/Sino05/labs/' not found
sinosheraliev@MacBook-Air-Dilshod laba % git push -u origin main
remote: Repository not found.
fatal: repository 'https://github.com/Sino05/labs/' not found
sinosheraliev@MacBook-Air-Dilshod laba % git push -u orig main  
To github.com:Sino05/LABA.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'github.com:Sino05/LABA.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
sinosheraliev@MacBook-Air-Dilshod laba % git push -u orig master
error: src refspec master does not match any
error: failed to push some refs to 'github.com:Sino05/LABA.git'
sinosheraliev@MacBook-Air-Dilshod laba % git branch
* main
sinosheraliev@MacBook-Air-Dilshod laba % git branch
* main
sinosheraliev@MacBook-Air-Dilshod laba % git push -u orig master
error: src refspec master does not match any
error: failed to push some refs to 'github.com:Sino05/LABA.git'
sinosheraliev@MacBook-Air-Dilshod laba % git push -u orig main  
To github.com:Sino05/LABA.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'github.com:Sino05/LABA.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
sinosheraliev@MacBook-Air-Dilshod laba % git pull
remote: Repository not found.
fatal: repository 'https://github.com/Sino05/labs/' not found
sinosheraliev@MacBook-Air-Dilshod laba % git remote set-url origin git@github.com:Sino05/LABA.git
sinosheraliev@MacBook-Air-Dilshod laba % git push
To github.com:Sino05/LABA.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'github.com:Sino05/LABA.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
sinosheraliev@MacBook-Air-Dilshod laba % git pull
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 582 bytes | 194.00 KiB/s, done.
From github.com:Sino05/LABA
 + 539ed09...b536f5d main       -> origin/main  (forced update)
hint: You have divergent branches and need to specify how to reconcile them.
hint: You can do so by running one of the following commands sometime before
hint: your next pull:
hint: 
hint:   git config pull.rebase false  # merge
hint:   git config pull.rebase true   # rebase
hint:   git config pull.ff only       # fast-forward only
hint: 
hint: You can replace "git config" with "git config --global" to set a default
hint: preference for all repositories. You can also pass --rebase, --no-rebase,
hint: or --ff-only on the command line to override the configured default per
hint: invocation.
fatal: Need to specify how to reconcile divergent branches.
sinosheraliev@MacBook-Air-Dilshod laba % git remote add origin git@github.com:Sino05/inf_labs.git
error: remote origin already exists.
sinosheraliev@MacBook-Air-Dilshod laba % git remote set-url origin git@github.com:Sino05/inf_labs.git
sinosheraliev@MacBook-Air-Dilshod laba % git status
On branch main
Your branch and 'origin/main' have diverged,
and have 2 and 1 different commits each, respectively.
  (use "git pull" to merge the remote branch into yours)

nothing to commit, working tree clean
sinosheraliev@MacBook-Air-Dilshod laba % git branch -M main
git push -u origin main
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (9/9), 2.36 KiB | 2.36 MiB/s, done.
Total 9 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:Sino05/inf_labs.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
sinosheraliev@MacBook-Air-Dilshod laba % git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
sinosheraliev@MacBook-Air-Dilshod laba % git push
Everything up-to-date
sinosheraliev@MacBook-Air-Dilshod laba % git add -all
error: did you mean `--all` (with two dashes)?
sinosheraliev@MacBook-Air-Dilshod laba % git add --all 
sinosheraliev@MacBook-Air-Dilshod laba % git commit -m "Изменения в стиле markdown"
[main d72e07d] Изменения в стиле markdown
 2 files changed, 50 insertions(+), 1 deletion(-)
sinosheraliev@MacBook-Air-Dilshod laba % git push
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 8 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 549 bytes | 549.00 KiB/s, done.
Total 5 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
To github.com:Sino05/inf_labs.git
   049174e..d72e07d  main -> main
sinosheraliev@MacBook-Air-Dilshod laba % git branch new-task
sinosheraliev@MacBook-Air-Dilshod laba % git checkout new-task
Switched to branch 'new-task'
sinosheraliev@MacBook-Air-Dilshod laba % git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.                                                                                       
```
7. **Замечания автора** отсутствует
8. **Выводы**: Я научился работать с git.Я научился связывать локольный и удаленный репозитории. Я научился мержить ветки в гите!
