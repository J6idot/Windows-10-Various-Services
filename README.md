# Windows 10 Services by J6idot
Welcome to my (sort of) little project on figuring out what services are needed for booting Windows 10 using the absolute bare minimum, and what services are required for each component.

----

## ABSOLUTE MINIMUM to get to the desktop
| Visible Service Name | Service Name | Start Type | Description |
| --- | --- | --- | --- |
| Background Tasks Infrastructure Service | BrokerInfrastructure | Automatic | ???? |
| CoreMessaging | CoreMessagingRegistrar | Automatic | ???? |
| DCOM Server Process Launcher | DcomLaunch | Automatic | Every service depends on this. |
| Local Session Manager | LSM | Automatic | ???? |
| Remote Procedure Call (RPC) | RpcSs | Automatic | Same as DcomLaunch. |
| RPC Endpoint Mapper | RpcEptMapper | Automatic | Same as DcomLaunch. |
| User Manager | UserManager | Automatic | ???? |
| User Profile Service | ProfSvc | Automatic | Needed to load the user profile. |

## Audio
| Visible Service Name | Service Name | Start Type | Description |
| --- | --- | --- | --- |
| Windows Audio | Audiosrv | Automatic | ???? |
| Windows Audio Endpoint Builder | AudioEndpointBuilder | Manual | ???? |

## Display
| Visible Service Name | Service Name | Start Type | Description |
| --- | --- | --- | --- |
| Display Enhancement Service | DisplayEnhancementService | Manual | Used for controlling the brightness. |
| Sensors Service | SensorService | Manual | ???? |
| Sensor Monitoring Service | SensrSvc | Manual | Used for autobrightness. |

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
| AppX Deployment Service (AppXSVC) | AppXSvc | Manual | Required to run downloaded UWP apps. |
| Capability Access Manager Service | camsvc | Manual | Fixes the missing name in settings app and probably fixes some other stuff. |
| Client License Service (ClipSVC) | ClipSvc | Manual | Same as AppXSvc. |
| State Repository Service | StateRepository | Manual | I highly recommend that you enable this. Without it, windows is pretty much unusable. |

## Microsoft Store
| Visible Service Name | Service Name | Start Type | Description |
| --- | --- | --- | --- |
| Microsoft Store Install Service | InstallService | Manual | Required or else the MS Store crashes. |

## WLAN
| Visible Service Name | Service Name | Start Type | Description |
| --- | --- | --- | --- |
| DHCP Client | Dhcp | Automatic | Used for establishing an IP Address automatically. |
| DNS Client | Dnscache | Automatic | Used for establishing the DNS address automatically. |
| Network Connected Devices Auto-Setup | NcdAutoSetup | Manual | Depends on WlanSvc. |
| Network List Service | netprofm | Manual | ???? |
| Network Location Awareness | NlaSvc | Automatic | Same as EventLog. |
| Network Store Interface Service | nsi | Automatic | ???? |
| Windows Event Log | EventLog | Automatic | This apparently makes the WIFI logo appear on the taskbar. |
| WLAN AutoConfig | WlanSvc | Automatic | Without this service, you can't view the networks available. |

