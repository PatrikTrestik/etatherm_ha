<a href="https://www.buymeacoffee.com/qG6DdXgzah" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-blue.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>

> **Deprecated — last release.** This integration uses the legacy Etatherm protocol and will not receive further features. Please migrate to **[Etatherm Modbus](https://github.com/PatrikTrestik/etatherm_modbus)** (Modbus TCP, UI config flow).

# Etatherm for Home Assistant
Repo contains custom integration for Etatherm heating (etatherm.cz)

## Migrate to Etatherm Modbus

1. Install [Etatherm Modbus](https://github.com/PatrikTrestik/etatherm_modbus) from HACS.
2. Remove `climate: - platform: etatherm` from `configuration.yaml`.
3. Restart Home Assistant.
4. Add **Etatherm Modbus** under **Settings → Devices & services**.

## Configuration
There is no config flow. YAML setup still works on this last release.

Write to configuration.yaml

    climate:
    - platform: etatherm
      host: IP of your Eth1eC/D or serial/TCP converter
      port: 50001 
      adr_a: 255
      adr_j: 1

### Serial connection support - not tested
    climate:
    - platform: etatherm
      serial: serial port of your Eth1mod (COMX on Windows /dev/ttyUSBX on Linux)
      baudrate: 9600 
      adr_a: 255
      adr_j: 1

Please let me know if this works. I have no testing hardware anymore.
