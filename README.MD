# NRF52840 + Openthread + Azure IoT Hub
`NRF52840` is connected via OpenThread to an docker instance of OpenThread `Border Router` (https://openthread.io/guides/border-router/docker) and communicates directly with Azure IoT Hub (https://learn.microsoft.com/en-us/azure/iot-hub/) via `Azure SDK FOR C` (https://github.com/nrfconnect/azure-sdk-for-c).
## SDKS used
Freestanding VSCode project see /.vscode/settings.json
```
{
    "nrf-connect.topdir": "${nrf-connect.sdk:2.2.0}",
    "nrf-connect.toolchain.path": "${nrf-connect.toolchain:2.2.0}",
    "nrf-connect.applications": [
        "${workspaceFolder}",
        "c:\\repos\\zephr_mqtt_azure"
    ],
    ...
}
```
## Code base
* `Thread CLI` as base: https://developer.nordicsemi.com/nRF_Connect_SDK/doc/latest/nrf/samples/openthread/cli/README.html
* `nRF9160: Azure IoT Hub` for Azure IoT Hub SDK Code: https://developer.nordicsemi.com/nRF_Connect_SDK/doc/latest/nrf/samples/nrf9160/azure_iot_hub/README.html#sampoutput-azure-iot
* `Azure IoT Hub` Configurations: https://developer.nordicsemi.com/nRF_Connect_SDK/doc/latest/nrf/libraries/networking/azure_iot_hub.html#azure-iot-hub-flash-certs
## How to build
Build, Flash and Monitor through VSCode NRF Connect Plugin UI