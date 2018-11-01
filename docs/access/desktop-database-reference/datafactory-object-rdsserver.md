---
title: DataFactory (objeto) (RDSServer)
TOCTitle: DataFactory Object (RDSServer)
ms:assetid: 1de76cdd-34dc-8547-29aa-48ad6067bdea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248971(v=office.15)
ms:contentKeyID: 48543605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8069ebf92f4603e5fe254a5b4c95e9c6f997a56f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870635"
---
# <a name="datafactory-object-rdsserver"></a>DataFactory (objeto) (RDSServer)


**Se aplica a**: Access 2013, Office 2013

Este objeto de negocio de servidor predeterminado implementa métodos que proporcionan acceso de lectura y escritura a orígenes de datos específicos para aplicaciones de cliente.

## <a name="remarks"></a>Comentarios

El objeto **RDSServer.DataFactory** se ha diseñado como objeto de automatización de servidor que recibe solicitudes de cliente. En una implementación de Internet, reside en un servidor web y el componente ADISAPI. El objeto **RDSServer.DataFactory** proporciona acceso de lectura y escritura a orígenes de datos especificados, pero no contiene lógica de validación ni de reglas de negocios.

Si utiliza un método que está disponible en los objetos **RDSServer.DataFactory** y [RDS.DataControl](datacontrol-object-rds.md), el servicio de datos remotos utiliza la versión de **RDS.DataControl** de forma predeterminada. En este caso, se supone un escenario de programación básico, en el que el objeto **RDSServer.DataFactory** actúa como objeto de negocio de servidor genérico.

Si desea que la aplicación web controle el procesamiento de servidor específico de tareas, puede reemplazar el **RDSServer.DataFactory** por un objeto de negocio personalizado.

Puede crear objetos de negocio de servidor que llamen a los métodos **RDSServer.DataFactory**, como [Query](query-method-rds.md) y [CreateRecordset](createrecordset-method-rds.md). Esto es muy útil si desea agregar funcionalidad a los objetos de negocio y aprovechar las ventajas de las tecnologías de servicios de datos remotos existentes.

El identificador de clase para el objeto **RDSServer.DataFactory** es 9381D8F5-0288-11D0-9501-00AA00B911A5.

