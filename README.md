# IoTHubFirmwareUpdate
IoT Hub device firmware update example using Direct Method and Device TWIN, including trigger application.

Initially built from tutorial: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-csharp-csharp-firmware-update

Two projects. 

<li>Trigger
<li>Device

<b>Trigger</b>

The trigger application sends updated device firmware requirements to the target device via a direct method call. It then reports back progress information received from the device during the upgrade process using device properties(TWIN).

<b>Device</b>

A simulated device which registers callbacks for receipt of device property changes. It acts on firmware update properties assigned to it via the <b>Trigger</B> application. Each step is simulated with a delay. Each step reports back progress using the device properties mechanism.

