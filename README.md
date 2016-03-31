Learning d3.js Mapping
======================

## Fix

I prefer local js file (the network sucks in china.), so...

```bash
perl -pi -e "s:http\://d3js\.org/topojson\.v1\.min\.js:../topojson.v1.min.js:" **/*.html
perl -pi -e "s:http\://d3js\.org/d3\.v3\.min\.js:d3.min.js:" **/*.html
rm **/*.bak
```

## koan

How could perl prevent us from editing a file inplace without a backup, I really need that.
Cause I can `git reset --hard HEAD` to revert. Not any backup protection needed.
