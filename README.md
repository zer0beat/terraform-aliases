# terraform-aliases

This repository contains [a script](generate_aliases.py) to generate hundreds of
convenient terraform aliases programmatically.

**NOTE: The foundation of this repository is based on the amazing work done in [kubectl-aliases](https://github.com/ahmetb/kubectl-aliases) project by [@ahmetb](https://twitter.com/ahmetb).**

### Examples

Some of the  generated aliases are:

```sh
alias tf='terraform'
alias tfa='terraform apply'
alias tfc='terraform console'
alias tfd='terraform destroy'
alias tff='terraform fmt'
alias tfg='terraform graph'
alias tfim='terraform import'
alias tfin='terraform init'
...
```

See [the full list](.terraform_aliases).

### Installation

You can directly download the [`.terraform_aliases` file](https://raw.githubusercontent.com/zer0beat/terraform-aliases/master/.terraform_aliases)
and save it in your $HOME directory, then edit your .bashrc/.zshrc file with:

```sh
[ -f ~/.terraform_aliases ] && source ~/.terraform_aliases
```

**Print the full command before running it:** Add this to your `.bashrc` or
`.zshrc` file:

```sh
function terraform() { echo "+ terraform $@"; command terraform $@; }
```
  
### FAQ

**Does this not slow down my shell start up?** Sourcing the file that contains
~500 aliases takes about 30-45 milliseconds in my shell (zsh). I don't think
it's a big deal for me. Measure it with `echo $(($(date +%s%N)/1000000))`
command yourself in your .bashrc/.zshrc.

### Authors

- [@ahmetb](https://twitter.com/ahmetb)
- [@zer0beat](https://twitter.com/zer0beat)
