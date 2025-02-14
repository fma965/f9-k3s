# F9-K3S
Kubernetes GitOps using [FluxCD](https://fluxcd.io/)

Check my [Wiki](https://wiki.f9.casa) for more details! (WIP)

All `secret.enc.yaml` and `*-secret.enc.yaml` files are encrypted with SOPS using AGE.

I have included `secret.sample.yaml` and `*-secret.sample.yaml` files which contain placeholder values to enhance the usability.

Set your GitHooks to use `.githooks` with this command
`git config --local core.hooksPath .githooks/`
This makes sure any filename with `secret.yaml` in it's name is encrypted with SOPS

[AGE](https://github.com/FiloSottile/age) keys for SOPS to use need to be saved in the following structure from the root of this repo.
`.sops/age/private.key` 
`.sops/age/public.key` 

Windows users download [SOPS](https://github.com/getsops/sops/releases/latest) and place it somewhere in your `PATH` (e.g. C:\Windows) otherwise secret encryption will not work

Linux users follow the instructions at [SOPS](https://github.com/getsops/sops/releases/latest) to install SOPS to `/usr/local/bin/sops`