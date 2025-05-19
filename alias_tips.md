How to create and cd to dir:
```
alias mkcd 'mkdir -p \!:1 && cd \!:1'
```

*Explanation:*

\!:1 refers to the first argument passed to the alias.

mkdir -p ensures parent directories are created if needed.

&& makes sure cd only runs if mkdir succeeds.

