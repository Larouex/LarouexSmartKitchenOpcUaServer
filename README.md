# Larouex Smart Kitchen OPCUA Server for Azure IoT Central Industrial IoT Scenarios
This project containerizes the Larouex Smart Kitchen OPC-UA Server for demonstration of Industrial IoT Scenarios for Azure IoT Central.

## Overview

We have created an "End to End" demonstration of the components that comprise a OPC-UA Server that integrates with Azure IoT Central for Telemetry and Visualizations. This is a contrived scenario that demonstrates a Smart Kitchen Scenario for Azure IoT Central.

## OPC Server Overview and Features

This is a OPC Server written in Python using the opcua-asyncio that is based on the popular FreeOpcUa project/library. We have added implementations to Azure IoT Central using the Azure IoT SDK for Python.

Here are links for reference (<i>no need to install anything yet</i>)

* [LINK: Azure IoT SDKs for Python](https://github.com/Azure/azure-iot-sdk-python)
* [LINK: opcua-asyncio](https://github.com/FreeOpcUa/opcua-asyncio)

One important thing to note as you work through the tutorial here: If you are coming from the IoT Device world, the terminology of OPC is very different and vice-versa from OPC to Azure IoT Central. I will give simple, high level explanations, but be aware of those differences. The easist way to think about the assumptions we are making in the context of this tutorial...

| OPC | Azure IoT | Represented in Azure IoT Central |
|---|---|---|
| Node | Device Interface | Interface in the Device Capability Model |
| Variable | Telemetry | Telemetry Items in the Device Interface  |
| OPC Server | Device | We represent the OPC Server as a Device in IoT Central  |

The OPC Server implements three Telemetry Scenarios

  * Twin
  * Asset Specific
  * Downstream Gateway Devices

