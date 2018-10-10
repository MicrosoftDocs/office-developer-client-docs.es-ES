---
title: DataFactory (objeto) (RDSServer)
TOCTitle: DataFactory Object (RDSServer)
ms:assetid: 1de76cdd-34dc-8547-29aa-48ad6067bdea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248971(v=office.15)
ms:contentKeyID: 48543605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba705854fc27a18fd0d3d7a7c6fd7acdefb3830f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483594"
---
# <a name="datafactory-object-rdsserver"></a><span data-ttu-id="8ce8f-102">DataFactory (objeto) (RDSServer)</span><span class="sxs-lookup"><span data-stu-id="8ce8f-102">DataFactory Object (RDSServer)</span></span>


<span data-ttu-id="8ce8f-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ce8f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8ce8f-104">Este objeto de negocio de servidor predeterminado implementa métodos que proporcionan acceso de lectura y escritura a orígenes de datos específicos para aplicaciones de cliente.</span><span class="sxs-lookup"><span data-stu-id="8ce8f-104">This default server-side business object implements methods that provide read/write data access to specified data sources for client-side applications.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ce8f-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8ce8f-105">Remarks</span></span>

<span data-ttu-id="8ce8f-p101">El objeto **RDSServer.DataFactory** se ha diseñado como objeto de automatización de servidor que recibe solicitudes de cliente. En una implementación de Internet, reside en un servidor web y el componente ADISAPI crea instancias del mismo. El objeto **RDSServer.DataFactory** proporciona acceso de lectura y escritura a orígenes de datos especificados, pero no contiene lógica de validación ni de reglas de negocios.</span><span class="sxs-lookup"><span data-stu-id="8ce8f-p101">The **RDSServer.DataFactory** object is designed as a server-side Automation object that receives client requests. In an Internet implementation, it resides on a Web server and is instantiated by the ADISAPI component. The **RDSServer.DataFactory** object provides read and write access to specified data sources, but doesn't contain any validation or business rules logic.</span></span>

<span data-ttu-id="8ce8f-p102">Si utiliza un método que está disponible en los objetos **RDSServer.DataFactory** y [RDS.DataControl](datacontrol-object-rds.md), el servicio de datos remotos utiliza la versión de **RDS.DataControl** de forma predeterminada. En este caso, se supone un escenario de programación básico, en el que el objeto **RDSServer.DataFactory** actúa como objeto de negocio de servidor genérico.</span><span class="sxs-lookup"><span data-stu-id="8ce8f-p102">If you use a method that is available in both the **RDSServer.DataFactory** and [RDS.DataControl](datacontrol-object-rds.md) objects, Remote Data Service uses the **RDS.DataControl** version by default. The default assumes a basic programming scenario, where the **RDSServer.DataFactory** serves as a generic server-side business object.</span></span>

<span data-ttu-id="8ce8f-111">Si desea que la aplicación Web controle el procesamiento de servidor específico de tareas, puede reemplazar el objeto **RDSServer.DataFactory** por un objeto de negocio personalizado.</span><span class="sxs-lookup"><span data-stu-id="8ce8f-111">If you want your Web application to handle task-specific server-side processing, you can replace the **RDSServer.DataFactory** with a custom business object.</span></span>

<span data-ttu-id="8ce8f-p103">Puede crear objetos de negocio de servidor que llamen a los métodos **RDSServer.DataFactory**, como [Query](query-method-rds.md) y [CreateRecordset](createrecordset-method-rds.md). Esto es muy útil si desea agregar funcionalidad a los objetos de negocio y aprovechar las ventajas de las tecnologías de servicios de datos remotos existentes.</span><span class="sxs-lookup"><span data-stu-id="8ce8f-p103">You can create server-side business objects that call the **RDSServer.DataFactory** methods, such as [Query](query-method-rds.md) and [CreateRecordset](createrecordset-method-rds.md). This is helpful if you want to add functionality to your business objects, but take advantage of existing Remote Data Service technologies.</span></span>

<span data-ttu-id="8ce8f-114">El identificador de clase para el objeto **RDSServer.DataFactory** es 9381D8F5-0288-11D0-9501-00AA00B911A5.</span><span class="sxs-lookup"><span data-stu-id="8ce8f-114">The class ID for the **RDSServer.DataFactory** object is 9381D8F5-0288-11D0-9501-00AA00B911A5.</span></span>
