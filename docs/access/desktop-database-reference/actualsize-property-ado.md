---
title: Propiedad ActualSize (ADO)
TOCTitle: ActualSize property (ADO)
ms:assetid: 020a414d-e6aa-5fb9-9b77-bd9d10124f8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15)
ms:contentKeyID: 48542949
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c13cb41299ddaf786e6412e43a50b1414ad818b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280435"
---
# <a name="actualsize-property-ado"></a><span data-ttu-id="e8429-102">Propiedad ActualSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="e8429-102">ActualSize property (ADO)</span></span>

<span data-ttu-id="e8429-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8429-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e8429-104">Indica la longitud real del valor de un campo.</span><span class="sxs-lookup"><span data-stu-id="e8429-104">Indicates the actual length of a field's value.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="e8429-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="e8429-105">Settings and return values</span></span>

<span data-ttu-id="e8429-p101">Devuelve un valor de tipo **Long**. Algunos proveedores pueden permitir la configuración de esta propiedad para reservar espacio para datos BLOB, en cuyo caso el valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="e8429-p101">Returns a **Long** value. Some providers may allow this property to be set to reserve space for BLOB data, in which case the default value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8429-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e8429-108">Remarks</span></span>

<span data-ttu-id="e8429-p102">Utilice la propiedad **ActualSize** para devolver la longitud real del valor de un objeto [Field](field-object-ado.md). La propiedad **ActualSize** es de sólo lectura para todos los campos. Si ADO no puede determinar la longitud del valor del objeto **Field**, la propiedad **ActualSize** devuelve **adUnknown**.</span><span class="sxs-lookup"><span data-stu-id="e8429-p102">Use the **ActualSize** property to return the actual length of a [Field](field-object-ado.md) object's value. For all fields, the **ActualSize** property is read-only. If ADO cannot determine the length of the **Field** object's value, the **ActualSize** property returns **adUnknown**.</span></span>

<span data-ttu-id="e8429-112">Las **propiedades ActualSize** y [DefinedSize](definedsize-property-ado.md) son diferentes.</span><span class="sxs-lookup"><span data-stu-id="e8429-112">The **ActualSize** and [DefinedSize](definedsize-property-ado.md) properties are different.</span></span> <span data-ttu-id="e8429-113">Un objeto **Field** con un tipo declarado de **adVarChar** y una longitud máxima de 50 caracteres devuelve 50 como valor de la propiedad **DefinedSize**, pero el valor que se devuelve para la propiedad **ActualSize** es la longitud de los datos almacenados en el campo del registro actual.</span><span class="sxs-lookup"><span data-stu-id="e8429-113">A **Field** object with a declared type of **adVarChar** and a maximum length of 50 characters returns a **DefinedSize** property value of 50, but the **ActualSize** property value it returns is the length of the data stored in the field for the current record.</span></span> <span data-ttu-id="e8429-114">Los objetos **Field** con un valor de **DefinedSize** mayor que 255 bytes se tratan como columnas de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="e8429-114">**Fields** with a **DefinedSize** greater than 255 bytes are treated as variable length columns.</span></span>

