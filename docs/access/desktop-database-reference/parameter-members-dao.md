---
title: Miembros del parámetro (DAO)
TOCTitle: Parameter Members
ms:assetid: 38e19de8-5318-6077-13b1-10653069aaeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192517(v=office.15)
ms:contentKeyID: 48544228
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cd6f2621b65a0584d79ef72bbba0341b8391ccf1
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937599"
---
# <a name="parameter-members-dao"></a><span data-ttu-id="2a029-102">Miembros del parámetro (DAO)</span><span class="sxs-lookup"><span data-stu-id="2a029-102">Parameter members (DAO)</span></span>


<span data-ttu-id="2a029-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a029-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2a029-p101">Un objeto Parameter representa un valor suministrado a una consulta. El parámetro está asociado con un objeto QueryDef creado a partir de una consulta de parámetros.</span><span class="sxs-lookup"><span data-stu-id="2a029-p101">A Parameter object represents a value supplied to a query. The parameter is associated with a QueryDef object created from a parameter query.</span></span>

## <a name="properties"></a><span data-ttu-id="2a029-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2a029-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2a029-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="2a029-107">Name</span></span></p></th>
<th><p><span data-ttu-id="2a029-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a029-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a029-109"><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></span><span class="sxs-lookup"><span data-stu-id="2a029-109"><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="2a029-p102">[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2a029-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="2a029-112">Establece o devuelve un valor que indica si un objeto <strong><a href="parameter-object-dao.md">Parameter</a></strong> representa un parámetro de entrada, un parámetro de salida, ambos o el valor devuelto del procedimiento (sólo áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="2a029-112">Sets or returns a value that indicates whether a <strong><a href="parameter-object-dao.md">Parameter</a></strong> object represents an input parameter, an output parameter, both, or the return value from the procedure (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a029-113"><strong><a href="parameter-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="2a029-113"><strong><a href="parameter-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2a029-p103">Devuelve el nombre del objeto especificado. <strong>String</strong> de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="2a029-p103">Returns the name of the specified object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a029-116"><strong><a href="parameter-properties-property-dao.md">Propiedades</a></strong></span><span class="sxs-lookup"><span data-stu-id="2a029-116"><strong><a href="parameter-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2a029-p104">Devuelve la colección <strong><a href="properties-collection-dao.md">Properties</a></strong> de un objeto especificado. solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2a029-p104">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a029-119"><strong><a href="parameter-type-property-dao.md">Tipo de</a></strong></span><span class="sxs-lookup"><span data-stu-id="2a029-119"><strong><a href="parameter-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2a029-p105">Establece un valor que indica el tipo operativo o de datos de un objeto. <strong>Integer</strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="2a029-p105">Sets or returns a value that indicates the operational type or data type of an object. Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a029-122"><strong><a href="parameter-value-property-dao.md">Valor</a></strong></span><span class="sxs-lookup"><span data-stu-id="2a029-122"><strong><a href="parameter-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2a029-p106">Establece o devuelve el valor de un objeto. <strong>Variant</strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="2a029-p106">Sets or returns the value of an object. Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

