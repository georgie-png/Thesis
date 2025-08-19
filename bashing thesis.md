
to symbolic link all the media folders locally

``` shell
sudo cp -r --symbolic-link /home/luck/Documents/syncd/Documents/Wiki/Thesis/Repo/0*/*media/ ../

```

symlink entries
``` shell
sudo cp --symbolic-link /home/luck/Documents/syncd/Documents/Wiki/Thesis/Repo/0*/*entries/0* ./

```


output thesis as pdf book

``` shell
pandoc --defaults ../pandoc_order.md --filter pandoc-fignos --filter pandoc-citeproc --toc --toc-depth=1 -V documentclass=memoir  -o ../../thesis_toc.pdf

```

make pandoc order
``` shell
echo "input-files:" >> ../pandoc_order.md
for file in ./*.md; do   if [[ "$file" != "./pandoc_order.md" ]];     then      echo "- $file" >> ../pandoc_order.md;   fi  done


```