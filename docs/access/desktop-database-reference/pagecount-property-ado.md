---
title: PageCount (propiedad, ADO)
TOCTitle: PageCount Property (ADO)
ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15)
ms:contentKeyID: 48546609
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5dcb984cd60d29939a96a7c3b81b17cc825faf46
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485949"
---
# <a name="pagecount-property-ado"></a><span data-ttu-id="d3b10-102">PageCount (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="d3b10-102">PageCount Property (ADO)</span></span>


<span data-ttu-id="d3b10-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3b10-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d3b10-104">Indica cuántas páginas de datos contiene el objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d3b10-104">Indicates how many pages of data the [Recordset](recordset-object-ado.md) object contains.</span></span>

## <a name="return-value"></a><span data-ttu-id="d3b10-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3b10-105">Return Value</span></span>

<span data-ttu-id="d3b10-106">Devuelve un valor de tipo **Long** que indica el número de páginas del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="d3b10-106">Returns a **Long** value that indicates the number of pages in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3b10-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d3b10-107">Remarks</span></span>

<span data-ttu-id="d3b10-108">Utilice la propiedad **NúmeroDePáginas (PageCount)** para determinar cuántas páginas de datos hay en el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="d3b10-108">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object.</span></span> <span data-ttu-id="d3b10-109">*Las páginas* son grupos de registros cuyo tamaño es igual que el valor de la propiedad [PageSize](pagesize-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d3b10-109">*Pages* are groups of records whose size equals the [PageSize](pagesize-property-ado.md) property setting.</span></span> <span data-ttu-id="d3b10-110">Aunque la última página esté incompleta debido a que existan menos registros que el valor **PageSize**, cuenta como una página adicional en el valor **NúmeroDePáginas (PageCount)**.</span><span class="sxs-lookup"><span data-stu-id="d3b10-110">Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value.</span></span> <span data-ttu-id="d3b10-111">Si el objeto **Recordset** no admite esta propiedad, el valor será -1 para indicar que **NúmeroDePáginas (PageCount)** es indeterminable.</span><span class="sxs-lookup"><span data-stu-id="d3b10-111">If the **Recordset** object does not support this property, the value will be -1 to indicate that the **PageCount** is indeterminable.</span></span>

<span data-ttu-id="d3b10-112">Vea las propiedades **PageSize** y [AbsolutePage](absolutepage-property-ado.md) para obtener más información acerca de la funcionalidad de las páginas.</span><span class="sxs-lookup"><span data-stu-id="d3b10-112">See the **PageSize** and [AbsolutePage](absolutepage-property-ado.md) properties for more on page functionality.</span></span>

