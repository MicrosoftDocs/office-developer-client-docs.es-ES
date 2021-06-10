---
title: Source (propiedad, Error de ADO)
TOCTitle: Source property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47ae7ea790265edc10be8c907869eefbe4e593ba
ms.sourcegitcommit: 66e74e39f44dca8c41f97f05528b8f9eb1aaed87
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "52061314"
---
# <a name="source-property-ado-error"></a><span data-ttu-id="4c564-102">Source (propiedad, Error de ADO)</span><span class="sxs-lookup"><span data-stu-id="4c564-102">Source property (ADO Error)</span></span>


<span data-ttu-id="4c564-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c564-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4c564-104">Indica el nombre del objeto o de la aplicación que ha generado un error originariamente.</span><span class="sxs-lookup"><span data-stu-id="4c564-104">Indicates the name of the object or application that originally generated an error.</span></span>

## <a name="return-value"></a><span data-ttu-id="4c564-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c564-105">Return value</span></span>

<span data-ttu-id="4c564-106">Devuelve un valor de tipo **String** que indica el nombre de un objeto o una aplicación.</span><span class="sxs-lookup"><span data-stu-id="4c564-106">Returns a **String** value that indicates the name of an object or application.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c564-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4c564-107">Remarks</span></span>

<span data-ttu-id="4c564-108">Utilice la propiedad **Source** de un objeto [Error](error-object-ado.md) para determinar el nombre del objeto o la aplicación que ha generado un error.</span><span class="sxs-lookup"><span data-stu-id="4c564-108">Use the **Source** property on an [Error](error-object-ado.md) object to determine the name of the object or application that originally generated an error.</span></span> <span data-ttu-id="4c564-109">Puede ser el nombre de clase o el Id. de programación del objeto.</span><span class="sxs-lookup"><span data-stu-id="4c564-109">This could be the object's class name or programmatic ID.</span></span> <span data-ttu-id="4c564-110">En los errores de ADO, el valor de la propiedad será **ADODB.**</span><span class="sxs-lookup"><span data-stu-id="4c564-110">For errors in ADO, the property value will be **ADODB.**</span></span> <span data-ttu-id="4c564-111">*ObjectName*, donde *ObjectName* es el nombre del objeto que ha desencadenado el error.</span><span class="sxs-lookup"><span data-stu-id="4c564-111">*ObjectName*, where *ObjectName* is the name of the object that triggered the error.</span></span> <span data-ttu-id="4c564-112">En ADOX y ADO MD, el valor será **ADOX.**</span><span class="sxs-lookup"><span data-stu-id="4c564-112">For ADOX and ADO MD, the value will be **ADOX.**</span></span> <span data-ttu-id="4c564-113">*ObjectName* y **ADOMD.**</span><span class="sxs-lookup"><span data-stu-id="4c564-113">*ObjectName* and **ADOMD.**</span></span> <span data-ttu-id="4c564-114">*ObjectName,* respectivamente.</span><span class="sxs-lookup"><span data-stu-id="4c564-114">*ObjectName,* respectively.</span></span>

<span data-ttu-id="4c564-115">Basándose en la documentación del error de las propiedades **Source**, [Number](number-property-ado.md) y [Description](description-property-ado.md) de los objetos **Error**, es posible escribir código que controle el error de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="4c564-115">Based on the error documentation from the **Source**, [Number](number-property-ado.md), and [Description](description-property-ado.md) properties of **Error** objects, you can write code that will handle the error appropriately.</span></span>

<span data-ttu-id="4c564-116">La propiedad **Source** es de sólo lectura para objetos **Error**.</span><span class="sxs-lookup"><span data-stu-id="4c564-116">The **Source** property is read-only for **Error** objects.</span></span>

