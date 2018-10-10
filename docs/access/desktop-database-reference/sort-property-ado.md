---
title: Sort (propiedad, ADO)
TOCTitle: Sort Property (ADO)
ms:assetid: f2a39b7f-8b96-cd1a-8248-71f8b867454a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250230(v=office.15)
ms:contentKeyID: 48548652
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f7e78357e2b662f5b94c2bbcbbe563e4001bcc56
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484006"
---
# <a name="sort-property-ado"></a><span data-ttu-id="a7db7-102">Sort (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="a7db7-102">Sort Property (ADO)</span></span>


<span data-ttu-id="a7db7-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a7db7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a7db7-104">Indica uno o más nombres de campo por los que se ordena el objeto [Recordset](recordset-object-ado.md), así como si el orden es ascendente o descendente.</span><span class="sxs-lookup"><span data-stu-id="a7db7-104">Indicates one or more field names on which the [Recordset](recordset-object-ado.md) is sorted, and whether each field is sorted in ascending or descending order.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a7db7-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="a7db7-105">Settings and Return Values</span></span>

<span data-ttu-id="a7db7-p101">Establece o devuelve un valor de tipo **String** que indica los nombres de campo del objeto **Recordset** que hay que ordenar. Cada nombre está separado por una coma y va seguido de forma opcional por un espacio en blanco y la palabra clave, **ASC**, que ordena el campo en orden ascendente o **DESC**, que lo hace por orden descendente. De forma predeterminada, si no se especifica palabra clave, el campo se ordena de forma ascendente.</span><span class="sxs-lookup"><span data-stu-id="a7db7-p101">Sets or returns a **String** value that indicates the field names in the **Recordset** on which to sort. Each name is separated by a comma, and is optionally followed by a blank and the keyword, **ASC**, which sorts the field in ascending order, or **DESC**, which sorts the field in descending order. By default, if no keyword is specified, the field is sorted in ascending order.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7db7-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a7db7-109">Remarks</span></span>

<span data-ttu-id="a7db7-p102">Esta propiedad exige que la propiedad [CursorLocation](cursorlocation-property-ado.md) se establezca en **adUseClient**. Si no existe un índice, se creará uno temporal para cada campo especificado en la propiedad **Sort**.</span><span class="sxs-lookup"><span data-stu-id="a7db7-p102">This property requires the [CursorLocation](cursorlocation-property-ado.md) property to be set to **adUseClient**. A temporary index will be created for each field specified in the **Sort** property if an index does not already exist.</span></span>

<span data-ttu-id="a7db7-112">La operación de ordenación es eficaz debido a que los datos no se reorganizan físicamente, sino que simplemente se obtiene acceso a ellos en el orden especificado por el índice.</span><span class="sxs-lookup"><span data-stu-id="a7db7-112">The sort operation is efficient because data is not physically rearranged, but is simply accessed in the order specified by the index.</span></span>

<span data-ttu-id="a7db7-p103">Si se establece la propiedad **Sort** en una cadena vacía, se restablecerá el orden original de todas las filas y se eliminarán los índices temporales. Los índices existentes no se eliminarán.</span><span class="sxs-lookup"><span data-stu-id="a7db7-p103">Setting the **Sort** property to an empty string will reset the rows to their original order and delete temporary indexes. Existing indexes will not be deleted.</span></span>

<span data-ttu-id="a7db7-115">Supongamos que un **objeto Recordset** contiene tres campos denominados *firstName*, *middleInitial*y *LastName (apellidos)*.</span><span class="sxs-lookup"><span data-stu-id="a7db7-115">Suppose a **Recordset** contains three fields named *firstName*, *middleInitial*, and *lastName*.</span></span> <span data-ttu-id="a7db7-116">Establezca la propiedad **Sort** en la cadena "lastName DESC, firstName ASC", que ordenará el **conjunto de registros** por apellidos en orden descendente, a continuación, por nombre en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="a7db7-116">Set the **Sort** property to the string, "lastName DESC, firstName ASC", which will order the **Recordset** by last name in descending order, then by first name in ascending order.</span></span> <span data-ttu-id="a7db7-117">La inicial media se omite.</span><span class="sxs-lookup"><span data-stu-id="a7db7-117">The middle initial is ignored.</span></span>

<span data-ttu-id="a7db7-p105">Ningún campo puede denominarse "ASC" ni "DESC", ya que esos nombres entran en conflicto con las palabras clave **ASC** y **DESC**. En los campos con nombres en conflicto, utilice un alias mediante la palabra clave **AS** de la consulta que devuelve el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a7db7-p105">No field can be named "ASC" or "DESC" because those names conflict with the keywords **ASC** and **DESC**. Give a field with a conflicting name an alias by using the **AS** keyword in the query that returns the **Recordset**.</span></span>

