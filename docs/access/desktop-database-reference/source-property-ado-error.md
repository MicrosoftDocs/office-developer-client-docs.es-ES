---
title: Source (propiedad, Error ADO)
TOCTitle: Source Property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dd8a2df4462d9f877d1b4451744fc51215227153
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875108"
---
# <a name="source-property-ado-error"></a><span data-ttu-id="fef60-102">Source (propiedad, Error ADO)</span><span class="sxs-lookup"><span data-stu-id="fef60-102">Source Property (ADO Error)</span></span>


<span data-ttu-id="fef60-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fef60-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fef60-104">Indica el nombre del objeto o de la aplicación que ha generado un error originariamente.</span><span class="sxs-lookup"><span data-stu-id="fef60-104">Indicates the name of the object or application that originally generated an error.</span></span>

## <a name="return-value"></a><span data-ttu-id="fef60-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fef60-105">Return value</span></span>

<span data-ttu-id="fef60-106">Devuelve un valor de tipo **String** que indica el nombre de un objeto o una aplicación.</span><span class="sxs-lookup"><span data-stu-id="fef60-106">Returns a **String** value that indicates the name of an object or application.</span></span>

## <a name="remarks"></a><span data-ttu-id="fef60-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fef60-107">Remarks</span></span>

<span data-ttu-id="fef60-108">Use la propiedad **Source** en un objeto [Error](error-object-ado.md) para determinar el nombre del objeto o la aplicación que generó originalmente un error.</span><span class="sxs-lookup"><span data-stu-id="fef60-108">Use the **Source** property on an [Error](error-object-ado.md) object to determine the name of the object or application that originally generated an error.</span></span> <span data-ttu-id="fef60-109">Esto podría ser el nombre de clase del objeto o el identificador de programación.</span><span class="sxs-lookup"><span data-stu-id="fef60-109">This could be the object's class name or programmatic ID.</span></span> <span data-ttu-id="fef60-110">Para los errores de ADO, el valor de la propiedad será \**ADODB. \*\*\* ObjectName*, donde *ObjectName* es el nombre del objeto que ha desencadenado el error.</span><span class="sxs-lookup"><span data-stu-id="fef60-110">For errors in ADO, the property value will be \**ADODB.\*\*\*ObjectName*, where *ObjectName* is the name of the object that triggered the error.</span></span> <span data-ttu-id="fef60-111">En ADOX y ADO MD, el valor será \**ADOX. \*\*\* ObjectName* y \**ADOMD. \*\*\* ObjectName,* respectivamente.</span><span class="sxs-lookup"><span data-stu-id="fef60-111">For ADOX and ADO MD, the value will be \**ADOX.\*\*\*ObjectName* and \**ADOMD.\*\*\*ObjectName,* respectively.</span></span>

<span data-ttu-id="fef60-112">Basándose en la documentación del error de las propiedades **Source**, [Number](number-property-ado.md) y [Description](description-property-ado.md) de los objetos **Error**, es posible escribir código que controle el error de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="fef60-112">Based on the error documentation from the **Source**, [Number](number-property-ado.md), and [Description](description-property-ado.md) properties of **Error** objects, you can write code that will handle the error appropriately.</span></span>

<span data-ttu-id="fef60-113">La propiedad **Source** es de sólo lectura para objetos **Error**.</span><span class="sxs-lookup"><span data-stu-id="fef60-113">The **Source** property is read-only for **Error** objects.</span></span>

