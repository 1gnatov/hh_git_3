```
git init
subl task3.txt
git hash-object -w task3.txt
git update-index --add --cacheinfo 100644 387394ca0e2e5bad9a8dcbbb7fa54685c568f06e task3.txt
git write-tree
echo "commit 1gnatov 1" | git commit-tree c4329e7672eaf5b16c54de736b7b5513d2b37ab8
git cat-file -p 163b44ca65607729397d5074b31e31ee4e99b787

subl task3.txt 
subl task3_new.txt
git hash-object -w task3.txt
git hash-object -w task3_new.txt
git update-index --add --cacheinfo 100644 f4db1cf412a6fbcb41e2a0d2319446bf2b64e420 task3.txt
git update-index --add --cacheinfo 100644 82ddefd212ee3d408250cf9ebe5c0f3cb113f08a task3_new.txt
git write-tree
echo "commit 1gnatov 2" | git commit-tree 9e4a41b -p 163b44c
git cat-file -p 5f3a295314b82912108e4f96366ee0def81f64da

git update-index --add --cacheinfo 100644 387394ca0e2e5bad9a8dcbbb7fa54685c568f06e gittask/task3.txt
git write-tree
echo "commit 1gnatov 3" | git commit-tree a926177 -p 5f3a295
git cat-file -p 190a32e8ce3eaee2076af6039d3aaf26ae425063
git log --stat 190a32e8ce3eaee2076af6039d3aaf26ae425063

echo "190a32e8ce3eaee2076af6039d3aaf26ae425063" > .git/refs/heads/master
git reset --hard HEAD
```
создал репу hh_git_3 https://github.com/1gnatov/hh_git_3/
```
git remote add origin git@github.com:1gnatov/hh_git_3.git
git push -u origin master
```
