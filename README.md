# Aviso
este repositorio es únicamente un copia y pega de 2 repositorios, esto lo hice para uso personal y también como respaldo en caso de que se deje de dar soporte a uno de los programas

---
[Affinity](<https://github.com/ryzendew/AffinityOnLinux>) & [LinOffice](<https://github.com/eylenburg/linoffice>)

---

# davinci resolve studio
## Enlace de [descarga](<https://swr.cloud.blackmagicdesign.com/DaVinciResolve/v20.3/DaVinci_Resolve_Studio_20.3_Linux.zip?verify=1764796277-a56ySl32M9Ko6DmezIVBa2VGxx7vo45DeZmaD9kP7Po%3D>)
#### descargar el repositorio descomprimirlo, luego ejecutas
`
DaVinci_Resolve_Studio_20.3_Linux.run
`

luego de instalarlo poner los siguientes comandos
`sudo pacman -S fuse2`

`cd /opt/resolve/libs && sudo mkdir disabled-libraries && sudo mv libglib* libgio* libgmodule* disabled-libraries`

`sudo /usr/bin/perl -pi -e 's/\x74\x11\xe8\x21\x23\x00\x00/\xeb\x11\xe8\x21\x23\x00\x00/g' /opt/resolve/bin/resolve`

`cd /opt/resolve
sudo perl -pi -e 's/\x03\x00\x89\x45\xFC\x83\x7D\xFC\x00\x74\x11\x48\x8B\x45\xC8\x8B/\x03\x00\x89\x45\xFC\x83\x7D\xFC\x00\xEB\x11\x48\x8B\x45\xC8\x8B/' bin/resolve
sudo perl -pi -e 's/\x74\x11\x48\x8B\x45\xC8\x8B\x55\xFC\x89\x50\x58\xB8\x00\x00\x00/\xEB\x11\x48\x8B\x45\xC8\x8B\x55\xFC\x89\x50\x58\xB8\x00\x00\x00/' bin/resolve
sudo perl -pi -e 's/\x41\xb6\x01\x84\xc0\x0f\x84\xb0\x00\x00\x00\x48\x85\xdb\x74\x08\x45\x31\xf6\xe9\xa3\x00\x00\x00/\x41\xb6\x00\x84\xc0\x0f\x84\xb0\x00\x00\x00\x48\x85\xdb\x74\x08\x45\x31\xf6\xe9\xa3\x00\x00\x00/' bin/resolve
echo -e "LICENSE blackmagic davinciresolvestudio 999999 permanent uncounted\n  hostid=ANY issuer=CGP customer=CGP issued=28-dec-2023\n  akey=0000-0000-0000-0000 _ck=00 sig=\"00\"" | sudo tee .license/blackmagic.lic`

Antes de abrir el programa visita la siguiente pagina
[ArchWIki](<https://wiki.archlinux.org/title/DaVinci_Resolve>) (de aqui vas a saber que opencl instalar dependiendo si tienes amd, nvidia o intel)
luego debes abrir davinci resolve luego apretas
`alt+f3` y luego agregan la propiedad global de ocultar decoracion de ventanas y ponen `no`, en caso de que tengas el applet de `menu global` y `window buttons` esto no es necesario
# Affinity
simplemente descargar y ejecutar, es automático

# linoffice
```
curl -sSL https://github.com/eylenburg/linoffice/raw/refs/heads/main/quickstart.sh -o quickstart.sh && chmod +x quickstart.sh && ./quickstart.sh
```
luego dentro de la aplicaron
```
irm https://get.activated.win | iex
```
