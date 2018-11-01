---
title: Number (propiedad, ADO)
TOCTitle: Number property (ADO)
ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15)
ms:contentKeyID: 48547243
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 72afba54062a3f103fe75939502c9f52eef4c44d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887203"
---
# <a name="number-property-ado"></a><span data-ttu-id="73591-102">Number (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="73591-102">Number property (ADO)</span></span>


<span data-ttu-id="73591-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="73591-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="73591-104">Indica el número que identifica de forma exclusiva a un objeto [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="73591-104">Indicates the number that uniquely identifies an [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="73591-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73591-105">Return value</span></span>

<span data-ttu-id="73591-106">Devuelve un valor de tipo **Long** que puede corresponder a una de las constantes [ErrorValueEnum](errorvalueenum.md).</span><span class="sxs-lookup"><span data-stu-id="73591-106">Returns a **Long** value that may correspond to one of the [ErrorValueEnum](errorvalueenum.md) constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="73591-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="73591-107">Remarks</span></span>

<span data-ttu-id="73591-p101">Utilice la propiedad **Number** para determinar el error que se ha producido. El valor de la propiedad es un número exclusivo que corresponde a la condición de error.</span><span class="sxs-lookup"><span data-stu-id="73591-p101">Use the **Number** property to determine which error occurred. The value of the property is a unique number that corresponds to the error condition.</span></span>

<span data-ttu-id="73591-110">La colección [Errors](errors-collection-ado.md) devuelve un HRESULT en formato hexadecimal (por ejemplo, 0x80004005) o en valor de tipo long (por ejemplo, 2147467259).</span><span class="sxs-lookup"><span data-stu-id="73591-110">The [Errors](errors-collection-ado.md) collection returns an HRESULT in either hexadecimal format (for example, 0x80004005) or long value (for example, 2147467259).</span></span> <span data-ttu-id="73591-111">Estos HRESULT pueden ser generados por los componentes subyacentes, como OLE DB o incluso el propio OLE.</span><span class="sxs-lookup"><span data-stu-id="73591-111">These HRESULTs can be raised by underlying components, such as OLE DB or even OLE itself.</span></span> <span data-ttu-id="73591-112">Para obtener más información acerca de estos números, consulte el capítulo 16 de la *referencia del programador de OLE DB.*</span><span class="sxs-lookup"><span data-stu-id="73591-112">For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

