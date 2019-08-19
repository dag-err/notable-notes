---
tags: [git]
title: git svn
created: '2019-07-30T06:19:49.249Z'
modified: '2019-08-19T13:38:20.913Z'
---

# git svn

`subversion`

## get author names
```sh
svn log --xml https://repo/svn/general | grep author | sort -u | perl -pe 's/.*>(.*?)<.*/$1 = /' > users.txt

svn log --xml https://repo/svn/general/joomla_portalv3/com_portal | grep author | sort -u | perl -pe 's/.*>(.*?)<.*/$1 = /'
```

## svn to git migraiton
```sh
git svn clone \
  --stdlayout \
  --no-metadata \
  --authors-file=users.txt svn://hostname/path dest_dir-tmp

git svn clone \
  --stdlayout \
  --no-metadata \
  --authors-file=users.txt \
  --prefix=origin/ https://repo/svn/general/joomla_portalv3/com_portal dest_dir-tmp

git svn clone \
  --authors-file=users.txt \
  --prefix=origin/ \
  --trunk=joomla_portalv3/com_portal https://repo/svn/general dest_dir-tmp
```

[how-to-migrate-svn-repository](http://stackoverflow.com/questions/79165/how-to-migrate-svn-repository-with-history-to-a-new-git-repository)