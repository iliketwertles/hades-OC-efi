# hades-OC-efi
**DO NOT DOWNLOAD** (hackintosh efi for my desktop)   
this is mainly for me to have a off-site backup however there are some funky things i did that i consider worth sharing  

# **DO NOT DOWNLOAD**
please :3  
you will only cause more problems if you install this, there is no promise to keep this up to date, it is just a working concept for me. i don't like gatekeeping information tho

## Specs
i5 3570s  
rx 580(2048sp)[lspci output]/rx 590 gme[glxinfo output]  
16gb ddr3 ram  
kingston ssd for storage in macos  
6 series motherboard, not sure chipset  
350W psu  
supported intel ethernet  

## Getting gpu working
this applies for some supported* amd gpus, for example, asus rx 580 2048sp  

what i did, flash vbios to a supported card  
**MAKE SURE YOU HAVE A 2ND GPU OR A IGPU THAT WORKS!!!**  
i flashed a msi rx 580 8gb vbios and it enabled acceleration, however i dont know exactly what card i have, this is a problem  
also ensure to always have a backup of your stock vbios incase you fuck up, it happens, prepare for it  
the tool i used was amdvbflash (google, i think its not totally public but dont quote me on that)

after that, you have to do some tomfoolery to fix the purple tint that happens with DVI -> HDMI
you can use Corpnewts ForceRGB tool (link at bottom) to force RGB colorspace instead of dvi's default(causes purple tint)

## Handling ivybridge igpu for modern macos
you have to either disable the igpu in bios (dangerous) or disable it with a bootarg you get from whatevergreen  
that boot arg is: `-wegnoigpu`
