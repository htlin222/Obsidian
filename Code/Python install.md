# Python Install

[Anaconda | Anaconda Distribution](https://www.anaconda.com/products/distribution)

```shell=
export PATH=$PATH:/Users/mac/opt/anaconda3/lib/python3.9:PATH

# !! Contents within this block are managed by 'conda init' !!
__conda_setup="$('/Users/your_username/opt/anaconda3/bin/conda' 'shell.bash' 'hook' 2> /dev/null)"
if [ $? -eq 0 ]; then
    eval "$__conda_setup"
else
    if [ -f "/Users/your_username/opt/anaconda3/etc/profile.d/conda.sh" ]; then
        . "/Users/your_username/opt/anaconda3/etc/profile.d/conda.sh"
    else
        export PATH="/Users/your_username/opt/anaconda3/bin:$PATH"
    fi
fi
unset __conda_setup
# <<< conda initialize <<<
```
