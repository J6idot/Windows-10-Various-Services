# Windows 10 Services by J6idot
Welcome to my (sort of) little project on figuring out what services are needed for booting Windows 10 using the absolute bare minimum, and what services are required for each component.

----

## ABSOLUTE MINIMUM to get to the desktop
| Visible Service Name | Service Name | Start Type | Description |
| --- | --- | --- | --- |
| Background Tasks Infrastructure Service | BrokerInfrastructure | Automatic | ???? |
| CoreMessaging | CoreMessagingRegistrar | Automatic | ???? |
| DCOM Server Process Launcher | DcomLaunch | Automatic | ???? |
| Local Session Manager | LSM | Automatic | ???? |
| Remote Procedure Call (RPC) | RpcSs | Automatic | ???? |
| RPC Endpoint Mapper | RpcEptMapper | Automatic | ???? |
| User Manager | UserManager | Automatic | ???? |
| User Profile Service | ProfSvc | Automatic | ???? |

## Display
| Visible Service Name | Service Name | Start Type | Description |
| --- | --- | --- | --- |
| Display Enhancement Service | DisplayEnhancementService | Manual | Used for controlling the brightness. |
| Sensors Service | SensorService | Manual | ???? |
| | SensrSvc | Manual | Used for autobrightess. |

## HID
| Visible Service Name | Service Name | Start Type | Description |
| --- | --- | --- | --- |
| Human Interface Device Service | hidserv | Manual | Makes the power button and volume buttons work. |

## UAC
| Visible Service Name | Service Name | Start Type | Description |
| --- | --- | --- | --- |
| Application Information | Appinfo | Manual | Needed for running taskmgr.exe and other admin apps. |

## UWP
| Visible Service Name | Service Name | Start Type | Description |
| --- | --- | --- | --- |
| State Repository Service | StateRepository | Manual | I highly recommend that you enable this. Without it, windows is pretty much unusable. |

## WLAN
| Visible Service Name | Service Name | Start Type | Description |
| --- | --- | --- | --- |
| DHCP Client | Dhcp | Automatic | Used for establishing an IP Address automatically. |
| DNS Client | Dnscache | Automatic | Used for establishing the DNS client automatically. |
| Network Connected Devices Auto-Setup | NcdAutoSetup | Manual | ???? |
| Network List Service | netprofm | Manual | ???? |
| Network Store Interface Service | nsi | Automatic | ???? |
| Windows Event Log | EventLog | Automatic | This apparently makes the WIFI logo appear on the taskbar. |
| WLAN AutoConfig | WlanSvc | Automatic | ???? |
| | NlaSvc | Automatic | Same as EventLog. |

