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
| RPC Endpoint Mapper | RpcEptMapper | Automatic | ???? |
| Remote Procedure Call (RPC) | RpcSs | Automatic | ???? |
| User Profile Service | ProfSvc | Automatic | ???? |
| User Manager | UserManager | Automatic | ???? |

## UAC
| Visible Service Name | Service Name | Start Type | Description |
| --- | --- | --- | --- |
| Application Information | Appinfo | Manual | Needed for running taskmgr.exe and other admin apps. |

## UWP
| Visible Service Name | Service Name | Start Type | Description |
| --- | --- | --- | --- |
| State Repository Service | StateRepository | Manual | I highly recommend that you enable this. Without it, windows is pretty much unusable.
