---
title: AllowNullsEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: AllowNullsEnum
ms:assetid: 7bb42b38-6b3b-5930-b1d7-16323a3bdf37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249515(v=office.15)
ms:contentKeyID: 48545819
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c184253551fa3f974de1840d47654af597881cb8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701434"
---
# <a name="allownullsenum"></a><span data-ttu-id="aafda-102">AllowNullsEnum</span><span class="sxs-lookup"><span data-stu-id="aafda-102">AllowNullsEnum</span></span>

<span data-ttu-id="aafda-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aafda-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aafda-104">Especifica si se indizan registros con valores nulos.</span><span class="sxs-lookup"><span data-stu-id="aafda-104">Specifies whether records with null values are indexed.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aafda-105">Constante</span><span class="sxs-lookup"><span data-stu-id="aafda-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="aafda-106">Valor</span><span class="sxs-lookup"><span data-stu-id="aafda-106">Value</span></span></p></th>
<th><p><span data-ttu-id="aafda-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="aafda-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aafda-108"><strong>adIndexNullsAllow</strong></span><span class="sxs-lookup"><span data-stu-id="aafda-108"><strong>adIndexNullsAllow</strong></span></span></p></td>
<td><p><span data-ttu-id="aafda-109">0</span><span class="sxs-lookup"><span data-stu-id="aafda-109">0</span></span></p></td>
<td><p><span data-ttu-id="aafda-p101">El índice sí permite entradas en las que las columnas clave son nulas.

Si se escribe un valor nulo en una columna clave, la entrada se inserta en el índice.</span><span class="sxs-lookup"><span data-stu-id="aafda-p101">The index does allow entries in which the key columns are null. If a null value is entered in a key column, the entry is inserted into the index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aafda-112"><strong>adIndexNullsDisallow</strong></span><span class="sxs-lookup"><span data-stu-id="aafda-112"><strong>adIndexNullsDisallow</strong></span></span></p></td>
<td><p><span data-ttu-id="aafda-113">1</span><span class="sxs-lookup"><span data-stu-id="aafda-113">1</span></span></p></td>
<td><p><span data-ttu-id="aafda-p102">Valor predeterminado.

El índice no permite entradas en las que las columnas clave son nulas.

Si se escribe un valor nulo en una columna clave, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="aafda-p102">Default. The index does not allow entries in which the key columns are null. If a null value is entered in a key column, an error will occur.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aafda-117"><strong>adIndexNullsIgnore</strong></span><span class="sxs-lookup"><span data-stu-id="aafda-117"><strong>adIndexNullsIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="aafda-118">2</span><span class="sxs-lookup"><span data-stu-id="aafda-118">2</span></span></p></td>
<td><p><span data-ttu-id="aafda-p103">El índice no inserta entradas que contengan claves nulas.

Si se escribe un valor nulo en una columna clave, la entrada se omite y no se produce ningún error.</span><span class="sxs-lookup"><span data-stu-id="aafda-p103">The index does not insert entries containing null keys. If a null value is entered in a key column, the entry is ignored and no error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aafda-121"><strong>adIndexNullsIgnoreAny</strong></span><span class="sxs-lookup"><span data-stu-id="aafda-121"><strong>adIndexNullsIgnoreAny</strong></span></span></p></td>
<td><p><span data-ttu-id="aafda-122">4</span><span class="sxs-lookup"><span data-stu-id="aafda-122">4</span></span></p></td>
<td><p><span data-ttu-id="aafda-p104">El índice no inserta entradas en las que alguna columna clave contenga un valor nulo.

Para un índice que tenga una clave de varias columnas, si se escribe un valor nulo en alguna columna, la entrada se omite y no se produce ningún error.</span><span class="sxs-lookup"><span data-stu-id="aafda-p104">The index does not insert entries where some key column has a null value. For an index having a multi-column key, if a null value is entered in some column, the entry is ignored and no error occurs.</span></span></p></td>
</tr>
</tbody>
</table>

