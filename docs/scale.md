# Scaling and Performance Testing
Whilst The Power is not designed to do scaling/performance/load testing it has some capabilities that can be used for this.

## Creating a "large" environment.

- 30 repos using `create-many-repos.sh`

```
./create-many-repos.sh  1.95s user 0.75s system 8% cpu 32.277 total
```

- 30 repos using python-create-many-repos-connection-reuse.py

```
time python3 python-create-many-repos-connection-reuse.py
python3 python-create-many-repos-connection-reuse.py  0.13s user 0.05s system 1% cpu 16.075 total
```

If you keep within the GitHub recommendations about [file sizes](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github) on your GitHub repos and total size of your repo then you'll probably never need to look at performance. If you don't do that then you probably have a host of other problems.
