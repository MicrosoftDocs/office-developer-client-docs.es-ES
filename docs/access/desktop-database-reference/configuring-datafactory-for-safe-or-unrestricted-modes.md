---
title: Configurar DataFactory para los modos seguros o no restringidos
TOCTitle: Configuring DataFactory for Safe or Unrestricted Modes
ms:assetid: 1516068f-1b02-3236-f6a9-9fdeff098e52
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248915(v=office.15)
ms:contentKeyID: 48543400
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: abb461473d15f163fac6ea00f2af5d39f7b40d0a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486395"
---
# <a name="configuring-datafactory-for-safe-or-unrestricted-modes"></a>Configurar DataFactory para los modos seguros o no restringidos


**Se aplica a**: Access 2013 | Office 2013

ADO se instala de forma predeterminada con una configuración "segura" para [RDSServer.DataFactory](datafactory-object-rdsserver.md). El modo seguro para componentes de servidor RDS significa lo siguiente:

1.  Se requiere un controlador con el RDSServer.DataFactory (mediante un valor de clave del Registro).

2.  El controlador predeterminado, msdfmap.handler, está registrado, presente en la lista de controladores seguros y marcado como el controlador predeterminado.

3.  El archivo Msdfmap.ini se instala en el directorio de Windows. Deberá configurar este archivo según sus necesidades antes de utilizar RDS en el modo de tres niveles.

Opcionalmente, puede configurar una instalación de **DataFactory** no restringida. **DataFactory** se puede utilizar directamente sin el controlador personalizado. Los usuarios pueden seguir utilizando un controlador personalizado modificando las cadenas de conexión, pero no es necesario. Para obtener más información sobre las implicaciones de utilizar el objeto **RDSServer.DataFactory**, vea [Proteger aplicaciones RDS](securing-rds-applications.md).

El archivo de Registro, handsafe.reg, se ha proporcionado para configurar las entradas de controlador del Registro para una configuración segura. Para un funcionamiento en modo seguro, ejecute handsafe.reg. El archivo de Registro, handunsf.reg, se ha proporcionado para configurar las entradas de controlador del Registro para una configuración segura. Para un funcionamiento en modo no restringido, ejecute handunsf.reg.

Después de ejecutar handsafe.reg o handunsf.reg, deberá detener y reiniciar el servicio de publicación Web en el servidor Web escribiendo los comandos siguientes en una ventana de comandos: "NET STOP W3SVC" y "NET START W3SVC".

Para obtener más información acerca del uso de la característica de personalización de controladores de RDS, vea el artículo técnico "Using the Customization Handler Feature in RDS 2.1" (en inglés).

