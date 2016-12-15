# Troubleshooting

## Removing packages from the PPA:

### Method 1: Using ppa-purge
In case of our stable PPA:
```{r, engine='bash'}
sudo apt update
sudo apt install ppa-purge
sudo ppa-purge ppa:thopiekar/cura
```
In case of our master PPA:
```{r, engine='bash'}
sudo apt update
sudo apt install ppa-purge
sudo ppa-purge ppa:thopiekar/cura-master
```
### Method 2: Using synaptic
Using Synaptic you can easily see where your installed packages are from.
In our case you can easily select the PPA and remove all packages from there.
For more info on using Synaptic search the web for manuals. There are enough around...
![ultimaker_synaptic](https://cloud.githubusercontent.com/assets/1847437/21223747/2cfb8984-c2c9-11e6-9b20-fe240d2eef15.png)

### Method 3: Apt-Pinning
An easy method for advanced users is to change the PPAs priority using APT pinning.
While choosing a low "Pin-Priority" you can even tell APT to avoid a repository, if needed.
Using a low here will tell APT to downgrade to the Ubuntu packages whenever possible.
