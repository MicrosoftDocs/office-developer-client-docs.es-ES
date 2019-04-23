---
title: Miembros de parámetro (DAO)
TOCTitle: Parameter Members
ms:assetid: 38e19de8-5318-6077-13b1-10653069aaeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192517(v=office.15)
ms:contentKeyID: 48544228
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25eae70d88307331c44983c4e7cbbcce3fe9d309
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288115"
---
# <a name="parameter-members-dao"></a><span data-ttu-id="9ce7c-102">Miembros de parámetro (DAO)</span><span class="sxs-lookup"><span data-stu-id="9ce7c-102">Parameter members (DAO)</span></span>

<span data-ttu-id="9ce7c-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ce7c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9ce7c-104">Un objeto Parameter representa un valor suministrado a una consulta.</span><span class="sxs-lookup"><span data-stu-id="9ce7c-104">A Parameter object represents a value supplied to a query.</span></span> <span data-ttu-id="9ce7c-105">El parámetro está asociado con un objeto QueryDef creado a partir de una consulta de parámetros.</span><span class="sxs-lookup"><span data-stu-id="9ce7c-105">The parameter is associated with a QueryDef object created from a parameter query.</span></span>

## <a name="properties"></a><span data-ttu-id="9ce7c-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9ce7c-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9ce7c-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="9ce7c-107">Name</span></span></p></th>
<th><p><span data-ttu-id="9ce7c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="9ce7c-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ce7c-109"><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ce7c-109"><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ce7c-110"><strong>Nota</strong>: no se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="9ce7c-110"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="9ce7c-111">Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="9ce7c-111">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="9ce7c-112">Establece o devuelve un valor que indica si un objeto <strong><a href="parameter-object-dao.md">Parameter</a></strong> representa un parámetro de entrada, un parámetro de salida, ambos o el valor devuelto del procedimiento (sólo áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="9ce7c-112">Sets or returns a value that indicates whether a <strong><a href="parameter-object-dao.md">Parameter</a></strong> object represents an input parameter, an output parameter, both, or the return value from the procedure (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce7c-113"><strong><a href="parameter-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ce7c-113"><strong><a href="parameter-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ce7c-114">Devuelve el nombre del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="9ce7c-114">Returns the name of the specified object.</span></span> <span data-ttu-id="9ce7c-115">Sólo lectura de la <strong>cadena</strong>.</span><span class="sxs-lookup"><span data-stu-id="9ce7c-115">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce7c-116"><strong><a href="parameter-properties-property-dao.md">Propiedades</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ce7c-116"><strong><a href="parameter-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ce7c-117">Devuelve la colección <strong><a href="properties-collection-dao.md">Properties</a></strong> de un objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="9ce7c-117">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="9ce7c-118">Sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="9ce7c-118">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce7c-119"><strong><a href="parameter-type-property-dao.md">Tipo</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ce7c-119"><strong><a href="parameter-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ce7c-120">Establece o devuelve un valor que indica el tipo operativo o el tipo de datos de un objeto.</span><span class="sxs-lookup"><span data-stu-id="9ce7c-120">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="9ce7c-121"><strong>Integer</strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="9ce7c-121">Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce7c-122"><strong><a href="parameter-value-property-dao.md">Value</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ce7c-122"><strong><a href="parameter-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ce7c-123">Establece o devuelve el valor de un objeto.</span><span class="sxs-lookup"><span data-stu-id="9ce7c-123">Sets or returns the value of an object.</span></span> <span data-ttu-id="9ce7c-124"><strong>Variant</strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="9ce7c-124">Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

