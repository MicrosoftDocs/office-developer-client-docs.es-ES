---
title: DataFactory (objeto) (RDSServer)
TOCTitle: DataFactory object (RDSServer)
ms:assetid: 1de76cdd-34dc-8547-29aa-48ad6067bdea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248971(v=office.15)
ms:contentKeyID: 48543605
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77cd06992ef0062859d0a1372d115f8e65246a5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294480"
---
# <a name="datafactory-object-rdsserver"></a>DataFactory (objeto) (RDSServer)


**Se aplica a:** Access 2013, Office 2013

Este objeto de negocio de servidor predeterminado implementa métodos que proporcionan acceso de lectura y escritura a orígenes de datos específicos para aplicaciones de cliente.

## <a name="remarks"></a>Comentarios

El objeto **RDSServer.DataFactory** se ha diseñado como objeto de automatización de servidor que recibe solicitudes de cliente. En una implementación de Internet, reside en un servidor Web y la crea el componente ADISAPI. El objeto **RDSServer.DataFactory** proporciona acceso de lectura y escritura a orígenes de datos especificados, pero no contiene lógica de validación ni de reglas de negocios.

Si utiliza un método que está disponible en los objetos **RDSServer.DataFactory** y [RDS.DataControl](datacontrol-object-rds.md), el servicio de datos remotos utiliza la versión de **RDS.DataControl** de forma predeterminada. En este caso, se supone un escenario de programación básico, en el que el objeto **RDSServer.DataFactory** actúa como objeto de negocio de servidor genérico.

Si desea que la aplicación web controle el procesamiento del lado servidor específico de la tarea, puede reemplazar el objeto **RDSServer. DataFactory** por un objeto de negocio personalizado.

Puede crear objetos de negocio de servidor que llamen a los métodos **RDSServer.DataFactory**, como [Query](query-method-rds.md) y [CreateRecordset](createrecordset-method-rds.md). Esto es muy útil si desea agregar funcionalidad a los objetos de negocio y aprovechar las ventajas de las tecnologías de servicios de datos remotos existentes.

El identificador de clase para el objeto **RDSServer.DataFactory** es 9381D8F5-0288-11D0-9501-00AA00B911A5.

