---
title: Number (propiedad, ADO)
TOCTitle: Number Property (ADO)
ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15)
ms:contentKeyID: 48547243
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4e9b048643b1892197f610ef6d53e6ba46b170d8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483326"
---
# <a name="number-property-ado"></a><span data-ttu-id="981b7-102">Number (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="981b7-102">Number Property (ADO)</span></span>


<span data-ttu-id="981b7-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="981b7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="981b7-104">Indica el número que identifica de forma exclusiva a un objeto [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="981b7-104">Indicates the number that uniquely identifies an [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="981b7-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="981b7-105">Return Value</span></span>

<span data-ttu-id="981b7-106">Devuelve un valor de tipo **Long** que puede corresponder a una de las constantes [ErrorValueEnum](errorvalueenum.md).</span><span class="sxs-lookup"><span data-stu-id="981b7-106">Returns a **Long** value that may correspond to one of the [ErrorValueEnum](errorvalueenum.md) constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="981b7-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="981b7-107">Remarks</span></span>

<span data-ttu-id="981b7-p101">Utilice la propiedad **Number** para determinar el error que se ha producido. El valor de la propiedad es un número exclusivo que corresponde a la condición de error.</span><span class="sxs-lookup"><span data-stu-id="981b7-p101">Use the **Number** property to determine which error occurred. The value of the property is a unique number that corresponds to the error condition.</span></span>

<span data-ttu-id="981b7-110">La colección [Errors](errors-collection-ado.md) devuelve un HRESULT en formato hexadecimal (por ejemplo, 0x80004005) o en valor de tipo long (por ejemplo, 2147467259).</span><span class="sxs-lookup"><span data-stu-id="981b7-110">The [Errors](errors-collection-ado.md) collection returns an HRESULT in either hexadecimal format (for example, 0x80004005) or long value (for example, 2147467259).</span></span> <span data-ttu-id="981b7-111">Estos HRESULT pueden ser generados por los componentes subyacentes, como OLE DB o incluso el propio OLE.</span><span class="sxs-lookup"><span data-stu-id="981b7-111">These HRESULTs can be raised by underlying components, such as OLE DB or even OLE itself.</span></span> <span data-ttu-id="981b7-112">Para obtener más información acerca de estos números, consulte el capítulo 16 de la *referencia del programador de OLE DB.*</span><span class="sxs-lookup"><span data-stu-id="981b7-112">For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

