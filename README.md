# Template
This repository is intended to provide a template for tex-based documents. So far, the template supports only documents in connection with Coburg University. 

# Prerequisites
The project based on the template is intended to be built by VS Code's LaTeX Workshop extension. In order for this to work, some applications are needed to built essential work (and some are needed for special packages like minted to work):

## Essential applications
- A working texlive installation
- Perl
- VS Code's LaTeX Workshop extension

## Other needed applications
- Python 3.X
- Python package Pygments

## Latex distro settings

### Tex Live 
In order to use the output directory setting you have to give latex permissions to write to any directory. This can be done like follows:
```bash
kpsewhich texmf.cnf
sudo nano $(kpsewhich texmf.cnf)
```
Add this line to the file:
```bash
openout_any = a
```

Update the settings
```bash
sudo mktexlsr
```

### MiKTeX
- Open the MiKTeX Console as administrator.
- Go to the Settings tab.
- Add or search for the config variable openout_any and set it to a.
- Click Apply and close.
- (Optional) Run initexmf --update-fndb in the command prompt if changes don’t apply.