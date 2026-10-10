# SkodaLnxCmd
This add-on provides access to the MySkoda API.
## Configuration
### SKODA_VIN
The 17-character VIN of the vehicle.
### SKODA_KEY
The API key from MySkoda.


# Config files

The plugin does not, as of now, support auto-setup. This as to be done manually. 

1. Install programs that able you to edit the config files.
   <br>Example: `Terminal` or `File Explorer`.
2. Download config file: <br> 
   https://raw.githubusercontent.com/mem76/skodaLnxCmd-ha-addon/refs/heads/master/skodalnxcmd/sample.skoda.yaml
3. Change host name to what you HA selected.
   Example: `local-skodalnxcmd-service` to `4edeb129-skodalnxcmd-service `
4. Create directory `packages` in the config dir.
5. Copy the file into this dir
6. Add include the dir in the main config file.

```yaml
homeassistant:
   packages: !include_dir_named packages
```