# esphome_rollerblind
ESPhome config for roller blind

Configen exponerar följande mot HomeAssistant:
- Sensor Wifi signal
- Sensor uptime
- Cover
  - Open
  - Close
  - Stopp
- Service
  - Control stepper
    ```
    service: esphome.blind_bedroom_downstairs_control_stepper
    target: 10000
    ```
  - Control stepper percent
  - Update global
