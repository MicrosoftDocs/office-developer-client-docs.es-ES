---
title: DefaultDatabase (propiedad, ADO)
TOCTitle: DefaultDatabase property (ADO)
ms:assetid: a35c5631-f9d9-e51f-950b-e52169830d94
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249757(v=office.15)
ms:contentKeyID: 48546784
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 01ca42ff738afe3a35cab6263cdae32ac256f3d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294151"
---
# <a name="defaultdatabase-property-ado"></a><span data-ttu-id="47ddb-102">DefaultDatabase (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="47ddb-102">DefaultDatabase property (ADO)</span></span>


<span data-ttu-id="47ddb-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="47ddb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="47ddb-104">Indica la base de datos predeterminada de un objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="47ddb-104">Indicates the default database for a [Connection](connection-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="47ddb-105">Valores de configuración y devueltos</span><span class="sxs-lookup"><span data-stu-id="47ddb-105">Settings and return values</span></span>

<span data-ttu-id="47ddb-106">Establece o devuelve un valor de tipo **String** que da como resultado el nombre de una base de datos que está disponible en el proveedor.</span><span class="sxs-lookup"><span data-stu-id="47ddb-106">Sets or returns a **String** value that evaluates to the name of a database available from the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="47ddb-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="47ddb-107">Remarks</span></span>

<span data-ttu-id="47ddb-108">Utilice la propiedad **DefaultDatabase** para establecer o devolver el nombre de la base de datos predeterminada en un objeto **Connection** específico.</span><span class="sxs-lookup"><span data-stu-id="47ddb-108">Use the **DefaultDatabase** property to set or return the name of the default database on a specific **Connection** object.</span></span>

<span data-ttu-id="47ddb-p101">Si hay una base de datos predeterminada, puede que las cadenas SQL utilicen una sintaxis incompleta para obtener acceso a los objetos de esa base de datos. Para obtener acceso a los objetos de una base de datos distinta de la especificada en la propiedad **DefaultDatabase**, los nombres de objeto deben incluir el nombre de la base de datos deseada. Tras establecer la conexión, el proveedor escribirá la información de la base de datos predeterminada en la propiedad **DefaultDatabase**. Algunos proveedores permiten sólo una base de datos por conexión, en cuyo caso no se puede cambiar el valor de la propiedad **DefaultDatabase**.</span><span class="sxs-lookup"><span data-stu-id="47ddb-p101">If there is a default database, SQL strings may use an unqualified syntax to access objects in that database. To access objects in a database other than the one specified in the **DefaultDatabase** property, you must qualify object names with the desired database name. Upon connection, the provider will write default database information to the **DefaultDatabase** property. Some providers allow only one database per connection, in which case you cannot change the **DefaultDatabase** property.</span></span>

<span data-ttu-id="47ddb-113">Es posible que algunos orígenes de datos y proveedores no admitan esta característica y devuelvan un error o una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="47ddb-113">Some data sources and providers may not support this feature, and may return an error or an empty string.</span></span>

<span data-ttu-id="47ddb-114">**Uso del servicio de datos remotos** Esta propiedad no está disponible en un objeto **Connection** de cliente.</span><span class="sxs-lookup"><span data-stu-id="47ddb-114">**Remote Data Service Usage**This property is not available on a client-side **Connection** object.</span></span>

