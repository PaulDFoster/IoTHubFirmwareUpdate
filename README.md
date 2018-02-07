# IoTHubFirmwareUpdate
IoT Hub device firmware update example using Device TWIN, including trigger application.

Initially built from tutorial: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-csharp-csharp-firmware-update

Two projects. 

<li>Trigger
<li>Device

<b>Trigger</b>

The trigger application sends updated device properties to the target device and then reports back progress information received from the device during the upgrade process using device properties.

<b>Device</b>

A simulated device which registers callbacks for receipt of device property changes. It acts on firmware update properties assigned to it via the <b>Trigger</B> application. Each step is simulated with a delay. Each step reports back progress using the device properties mechanism.

