---
title: Propiedad DataSource (ADO)
TOCTitle: DataSource property (ADO)
ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15)
ms:contentKeyID: 48545087
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0dec30715d1eb4e31d7490db4cedd015ecf3c040
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294473"
---
# <a name="datasource-property-ado"></a><span data-ttu-id="34a02-102">Propiedad DataSource (ADO)</span><span class="sxs-lookup"><span data-stu-id="34a02-102">DataSource property (ADO)</span></span>


<span data-ttu-id="34a02-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="34a02-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="34a02-104">Indica un objeto que contiene los datos que se van a representar como un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="34a02-104">Indicates an object that contains data to be represented as a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="34a02-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="34a02-105">Remarks</span></span>

<span data-ttu-id="34a02-p101">Esta propiedad se usa para crear controles enlazados a datos con el Entorno de datos. El Entorno de datos mantiene colecciones de datos (orígenes de datos) que contienen objetos con nombre (*miembros de datos*) que se representarán como un objeto **Recordset**. </span><span class="sxs-lookup"><span data-stu-id="34a02-p101">This property is used to create data-bound controls with the Data Environment. The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a **Recordset** object *.*</span></span>

<span data-ttu-id="34a02-108">Las propiedades [DataMember](datamember-property-ado.md) y **DataSource** deben utilizarse conjuntamente.</span><span class="sxs-lookup"><span data-stu-id="34a02-108">The [DataMember](datamember-property-ado.md) and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="34a02-109">El objeto al que se hace referencia debe implementar la interfaz **IDataSource** y contener una interfaz **IRowset**.</span><span class="sxs-lookup"><span data-stu-id="34a02-109">The object referenced must implement the **IDataSource** interface and must contain an **IRowset** interface.</span></span>

<span data-ttu-id="34a02-110">**Uso**</span><span class="sxs-lookup"><span data-stu-id="34a02-110">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
