---
title: AllowNullsEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: AllowNullsEnum
ms:assetid: 7bb42b38-6b3b-5930-b1d7-16323a3bdf37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249515(v=office.15)
ms:contentKeyID: 48545819
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 04e67584e0f0c2eeb5a12e34fdf98a84cc1da852
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485006"
---
# <a name="allownullsenum"></a><span data-ttu-id="34a83-102">AllowNullsEnum</span><span class="sxs-lookup"><span data-stu-id="34a83-102">AllowNullsEnum</span></span>


<span data-ttu-id="34a83-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="34a83-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="34a83-104">Especifica si se indizan registros con valores nulos.</span><span class="sxs-lookup"><span data-stu-id="34a83-104">Specifies whether records with null values are indexed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="34a83-105">Constante</span><span class="sxs-lookup"><span data-stu-id="34a83-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="34a83-106">Valor</span><span class="sxs-lookup"><span data-stu-id="34a83-106">Value</span></span></p></th>
<th><p><span data-ttu-id="34a83-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="34a83-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34a83-108"><strong>adIndexNullsAllow</strong></span><span class="sxs-lookup"><span data-stu-id="34a83-108"><strong>adIndexNullsAllow</strong></span></span></p></td>
<td><p><span data-ttu-id="34a83-109">0</span><span class="sxs-lookup"><span data-stu-id="34a83-109">0</span></span></p></td>
<td><p><span data-ttu-id="34a83-p101">El índice sí permite entradas en las que las columnas clave son nulas.

Si se escribe un valor nulo en una columna clave, la entrada se inserta en el índice.</span><span class="sxs-lookup"><span data-stu-id="34a83-p101">The index does allow entries in which the key columns are null. If a null value is entered in a key column, the entry is inserted into the index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34a83-112"><strong>adIndexNullsDisallow</strong></span><span class="sxs-lookup"><span data-stu-id="34a83-112"><strong>adIndexNullsDisallow</strong></span></span></p></td>
<td><p><span data-ttu-id="34a83-113">1</span><span class="sxs-lookup"><span data-stu-id="34a83-113">1</span></span></p></td>
<td><p><span data-ttu-id="34a83-p102">Valor predeterminado.

El índice no permite entradas en las que las columnas clave son nulas.

Si se escribe un valor nulo en una columna clave, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="34a83-p102">Default. The index does not allow entries in which the key columns are null. If a null value is entered in a key column, an error will occur.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34a83-117"><strong>adIndexNullsIgnore</strong></span><span class="sxs-lookup"><span data-stu-id="34a83-117"><strong>adIndexNullsIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="34a83-118">2</span><span class="sxs-lookup"><span data-stu-id="34a83-118">2</span></span></p></td>
<td><p><span data-ttu-id="34a83-p103">El índice no inserta entradas que contengan claves nulas.

Si se escribe un valor nulo en una columna clave, la entrada se omite y no se produce ningún error.</span><span class="sxs-lookup"><span data-stu-id="34a83-p103">The index does not insert entries containing null keys. If a null value is entered in a key column, the entry is ignored and no error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34a83-121"><strong>adIndexNullsIgnoreAny</strong></span><span class="sxs-lookup"><span data-stu-id="34a83-121"><strong>adIndexNullsIgnoreAny</strong></span></span></p></td>
<td><p><span data-ttu-id="34a83-122">4</span><span class="sxs-lookup"><span data-stu-id="34a83-122">4</span></span></p></td>
<td><p><span data-ttu-id="34a83-p104">El índice no inserta entradas en las que alguna columna clave contenga un valor nulo.

Para un índice que tenga una clave de varias columnas, si se escribe un valor nulo en alguna columna, la entrada se omite y no se produce ningún error.</span><span class="sxs-lookup"><span data-stu-id="34a83-p104">The index does not insert entries where some key column has a null value. For an index having a multi-column key, if a null value is entered in some column, the entry is ignored and no error occurs.</span></span></p></td>
</tr>
</tbody>
</table>
