CONQUERE DE MONBRISON TITOUAN b1 dev

## 1.1 

git init
echo "Commit 0" > README.md
git add README.md
git commit -m "Commit 0"

echo "Commit 1" > README.md
git add README.md
git commit -m "Commit 1"
echo "Commit 4" > README.md
git add README.md
git commit -m "Commit 4"
echo "Commit 5" > README.md
git add README.md
git commit -m "Commit 5"
git checkout -b branch-1
echo "Commit 2" > README.md
git add README.md
git commit -m "Commit 2"
echo "Commit 3" > README.md
git add README.md
git commit -m "Commit 3"
git checkout main
git merge branch-1 -m "Fusion de branch-1 dans main"

git log --all --decorate --oneline --graph > reponses-exo-1.md

## 1.2 

git checkout -b branch-2
echo "Commit 9" > README.md
git add README.md
git commit -m "Commit 9"
echo "Commit 10" > README.md
git add README.md
git commit -m "Commit 10"

git log --all --decorate --oneline --graph >> reponses-exo-1.md

## 1.3

git rebase --onto main branch-2 branch-2

git log --all --decorate --oneline --graph >> reponses-exo-1.md

## 1.4

git checkout main
git merge branch-2

git log --all --decorate --oneline --graph >> reponses-exo-1.md

## 1.5

sed -i '/reponses-exo-1.md/d' .gitignore
git add reponses-exo-1.md
git commit -m "Réponses exercice 1"

git push origin main

