# Etatherm for Home Assistant
Repo contains custom integration for Etatherm heating (etatherm.cz)

## Configuration
There is no config flow yet.
Write to configuration.yaml

climate:
- platform: etatherm
  host: IP of your Eth1eC/D or serial/TCP converter
  port: 50001 