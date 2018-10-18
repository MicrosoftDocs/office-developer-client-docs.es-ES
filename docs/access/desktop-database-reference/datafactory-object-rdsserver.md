---
title: DataFactory (objeto) (RDSServer)
TOCTitle: DataFactory Object (RDSServer)
ms:assetid: 1de76cdd-34dc-8547-29aa-48ad6067bdea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248971(v=office.15)
ms:contentKeyID: 48543605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2249ea154ac40b9114dd3dab8006a6d26539adff
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605663"
---
# <a name="datafactory-object-rdsserver"></a>DataFactory (objeto) (RDSServer)


**Se aplica a**: Access 2013 | Office 2013

Este objeto de negocio de servidor predeterminado implementa métodos que proporcionan acceso de lectura y escritura a orígenes de datos específicos para aplicaciones de cliente.

## <a name="remarks"></a>Comentarios

<<<<<<< HEAD el objeto **RDSServer.DataFactory** está diseñado como un objeto de automatización del lado del servidor que recibe solicitudes de cliente. En una implementación de Internet, reside en un servidor web y el componente ADISAPI crea instancias del mismo. El objeto **RDSServer.DataFactory** proporciona acceso de lectura y escritura a orígenes de datos especificados, pero no contiene lógica de validación ni de reglas de negocios.

Si utiliza un método que está disponible en los objetos **RDSServer.DataFactory** y [RDS.DataControl](datacontrol-object-rds.md), el servicio de datos remotos utiliza la versión de **RDS.DataControl** de forma predeterminada. En este caso, se supone un escenario de programación básico, en el que el objeto **RDSServer.DataFactory** actúa como objeto de negocio de servidor genérico.

<a name="if-you-want-your-web-application-to-handle-task-specific-server-side-processing-you-can-replace-the-rdsserverdatafactory-with-a-custom-business-object"></a>Si desea que la aplicación Web controle el procesamiento de servidor específico de tareas, puede reemplazar el objeto **RDSServer.DataFactory** por un objeto de negocio personalizado.
=======
El objeto **RDSServer.DataFactory** se ha diseñado como objeto de automatización de servidor que recibe solicitudes de cliente. En una implementación de Internet, reside en un servidor web y el componente ADISAPI. El objeto **RDSServer.DataFactory** proporciona acceso de lectura y escritura a orígenes de datos especificados, pero no contiene lógica de validación ni de reglas de negocios.

Si utiliza un método que está disponible en los objetos **RDSServer.DataFactory** y [RDS.DataControl](datacontrol-object-rds.md), el servicio de datos remotos utiliza la versión de **RDS.DataControl** de forma predeterminada. En este caso, se supone un escenario de programación básico, en el que el objeto **RDSServer.DataFactory** actúa como objeto de negocio de servidor genérico.

Si desea que la aplicación web controle el procesamiento de servidor específico de tareas, puede reemplazar el **RDSServer.DataFactory** por un objeto de negocio personalizado.
>>>>>>> master

Puede crear objetos de negocio de servidor que llamen a los métodos **RDSServer.DataFactory**, como [Query](query-method-rds.md) y [CreateRecordset](createrecordset-method-rds.md). Esto es muy útil si desea agregar funcionalidad a los objetos de negocio y aprovechar las ventajas de las tecnologías de servicios de datos remotos existentes.

El identificador de clase para el objeto **RDSServer.DataFactory** es 9381D8F5-0288-11D0-9501-00AA00B911A5.

