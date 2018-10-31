---
title: Configurar DataFactory para los modos seguros o no restringidos
TOCTitle: Configuring DataFactory for Safe or Unrestricted Modes
ms:assetid: 1516068f-1b02-3236-f6a9-9fdeff098e52
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248915(v=office.15)
ms:contentKeyID: 48543400
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 04964b085d6ece60bbdb30e4561e6e02de76268d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863937"
---
# <a name="configuring-datafactory-for-safe-or-unrestricted-modes"></a><span data-ttu-id="7cfb8-102">Configurar DataFactory para los modos seguros o no restringidos</span><span class="sxs-lookup"><span data-stu-id="7cfb8-102">Configuring DataFactory for Safe or Unrestricted Modes</span></span>


<span data-ttu-id="7cfb8-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7cfb8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7cfb8-p101">ADO se instala de forma predeterminada con una configuración "segura" para [RDSServer.DataFactory](datafactory-object-rdsserver.md). El modo seguro para componentes de servidor RDS significa lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7cfb8-p101">By default, ADO is installed with a "safe" [RDSServer.DataFactory](datafactory-object-rdsserver.md) configuration. Safe mode for RDS Server components means that the following are true:</span></span>

1.  <span data-ttu-id="7cfb8-106">Se requiere un controlador con el RDSServer.DataFactory (mediante un valor de clave del Registro).</span><span class="sxs-lookup"><span data-stu-id="7cfb8-106">Handler is required with the RDSServer.DataFactory (this is mandated by a registry key setting).</span></span>

2.  <span data-ttu-id="7cfb8-107">El controlador predeterminado, msdfmap.handler, está registrado, presente en la lista de controladores seguros y marcado como el controlador predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7cfb8-107">The default handler, msdfmap.handler, is registered, present in the safe-handler list, and marked as the default handler.</span></span>

3.  <span data-ttu-id="7cfb8-p102">El archivo Msdfmap.ini se instala en el directorio de Windows. Deberá configurar este archivo según sus necesidades antes de utilizar RDS en el modo de tres niveles.</span><span class="sxs-lookup"><span data-stu-id="7cfb8-p102">Msdfmap.ini file is installed in the Windows directory. You must configure this file according to your needs, before using RDS in three-tier mode.</span></span>

<span data-ttu-id="7cfb8-110">Opcionalmente, puede configurar una instalación de **DataFactory** no restringida.</span><span class="sxs-lookup"><span data-stu-id="7cfb8-110">Optionally, you can configure an unrestricted **DataFactory** installation.</span></span> <span data-ttu-id="7cfb8-111">**DataFactory** se puede utilizar directamente sin el controlador personalizado.</span><span class="sxs-lookup"><span data-stu-id="7cfb8-111">**DataFactory** can be used directly without the custom handler.</span></span> <span data-ttu-id="7cfb8-112">Los usuarios pueden seguir utilizando un controlador personalizado modificando las cadenas de conexión, pero no es necesario.</span><span class="sxs-lookup"><span data-stu-id="7cfb8-112">Users can still use a custom handler by modifying the connection strings, but it is not required.</span></span> <span data-ttu-id="7cfb8-113">Para obtener más información acerca de las implicaciones de utilizar el objeto **RDSServer.DataFactory** , vea [Proteger aplicaciones RDS](securing-rds-applications.md).</span><span class="sxs-lookup"><span data-stu-id="7cfb8-113">For more information about the implications of using the **RDSServer.DataFactory** object, see [Securing RDS Applications](securing-rds-applications.md).</span></span>

<span data-ttu-id="7cfb8-p104">El archivo de Registro, handsafe.reg, se ha proporcionado para configurar las entradas de controlador del Registro para una configuración segura. Para un funcionamiento en modo seguro, ejecute handsafe.reg. El archivo de Registro, handunsf.reg, se ha proporcionado para configurar las entradas de controlador del Registro para una configuración segura. Para un funcionamiento en modo no restringido, ejecute handunsf.reg.</span><span class="sxs-lookup"><span data-stu-id="7cfb8-p104">The registry file handsafe.reg has been provided to set up the handler registry entries for a safe configuration. To run in safe mode, run handsafe.reg. The registry file handunsf.reg has been provided to set up the handler registry entries for an unrestricted configuration. To run in unrestricted mode, run handunsf.reg.</span></span>

<span data-ttu-id="7cfb8-117"><<<<<<< HEAD después de ejecutar handsafe.reg o handunsf.reg, debe detener y reiniciar el servicio de publicación World Wide Web en el servidor Web, escriba los siguientes comandos en una ventana de comandos: "NET detener W3SVC" y "NET iniciar W3SVC".</span><span class="sxs-lookup"><span data-stu-id="7cfb8-117"><<<<<<< HEAD After running either handsafe.reg or handunsf.reg, you must stop and restart the World Wide Web Publishing Service on the Web server by typing the following commands in a command window: "NET STOP W3SVC" and "NET START W3SVC".</span></span>
<span data-ttu-id="7cfb8-118">=== Después de ejecutar handsafe.reg o handunsf.reg, debe detener y reiniciar el servicio de publicación World Wide Web en el servidor web, escriba los siguientes comandos en una ventana de comandos: "NET detener W3SVC" y "NET iniciar W3SVC".</span><span class="sxs-lookup"><span data-stu-id="7cfb8-118">======= After running either handsafe.reg or handunsf.reg, you must stop and restart the World Wide Web Publishing Service on the web server by typing the following commands in a command window: "NET STOP W3SVC" and "NET START W3SVC".</span></span>
>>>>>>> <span data-ttu-id="7cfb8-119">master</span><span class="sxs-lookup"><span data-stu-id="7cfb8-119">master</span></span>

<span data-ttu-id="7cfb8-120">Para obtener más información acerca del uso de la característica de personalización de controladores de RDS, vea el artículo técnico "Using the Customization Handler Feature in RDS 2.1" (en inglés).</span><span class="sxs-lookup"><span data-stu-id="7cfb8-120">For more information about using the customization handler feature of RDS, see the technical article Using the Customization Handler Feature in RDS 2.1.</span></span>

