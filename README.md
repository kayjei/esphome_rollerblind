# esphome_rollerblind
ESPhome config for roller blind

Denna config skriver till NodeMcu flash-minne vid varje stopp, vilket förkortar NodeMcus livslängd. NodeMcu klarar ca 100.000 skrivningar

Configen exponerar följande mot HomeAssistant:
- Sensor Wifi signal
- Sensor uptime
- Cover
  - Open
  - Close
  - Stopp
- Service
  - Control stepper (Sätt ett mål för rullgardinen)
    ```
    service: esphome.${name}_control_stepper
    target: 10000
    ```
  - Control stepper percent (Sätt ett mål i procent för rullgardinen, där 100 är öppen och 0 är stängd)
    ```
    service: esphome.${name}_control_stepper_percent
    percent: 50
    ```
  - Update global (Uppdatera nuvarande position)
    ```
    service: esphome.${name}_update_global
    value: 10000
    ```
