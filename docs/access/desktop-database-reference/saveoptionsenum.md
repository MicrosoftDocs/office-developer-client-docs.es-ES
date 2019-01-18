---
title: SaveOptionsEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: SaveOptionsEnum
ms:assetid: 2a4e4c7a-6331-7270-0514-cc549c721ffd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249053(v=office.15)
ms:contentKeyID: 48543906
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77a617dc54d8acd145648d926e10cf7c9a3cf252
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705998"
---
# <a name="saveoptionsenum"></a><span data-ttu-id="29fd6-102">SaveOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="29fd6-102">SaveOptionsEnum</span></span>

<span data-ttu-id="29fd6-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="29fd6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="29fd6-p101">Especifica si un archivo se debe crear o sobrescribir al guardar desde un objeto [Stream](stream-object-ado.md). Los valores se pueden combinar con un operador AND (Y).</span><span class="sxs-lookup"><span data-stu-id="29fd6-p101">Specifies whether a file should be created or overwritten when saving from a [Stream](stream-object-ado.md) object. The values can be combined with an AND operator.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="29fd6-106">Constante</span><span class="sxs-lookup"><span data-stu-id="29fd6-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="29fd6-107">Valor</span><span class="sxs-lookup"><span data-stu-id="29fd6-107">Value</span></span></p></th>
<th><p><span data-ttu-id="29fd6-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="29fd6-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="29fd6-109"><strong>adSaveCreateNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="29fd6-109"><strong>adSaveCreateNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="29fd6-110">1</span><span class="sxs-lookup"><span data-stu-id="29fd6-110">1</span></span></p></td>
<td><p><span data-ttu-id="29fd6-p102">Valor predeterminado. Crea un archivo nuevo si el archivo especificado por el parámetro <em>FileName</em> aún no existe.</span><span class="sxs-lookup"><span data-stu-id="29fd6-p102">Default. Creates a new file if the file specified by the <em>FileName</em> parameter does not already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29fd6-113"><strong>adSaveCreateOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="29fd6-113"><strong>adSaveCreateOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="29fd6-114">2</span><span class="sxs-lookup"><span data-stu-id="29fd6-114">2</span></span></p></td>
<td><p><span data-ttu-id="29fd6-115">Si el archivo especificado por el parámetro <em>FileName</em> ya existe, se sobrescribe el archivo con los datos del objeto <strong>Stream</strong> actualmente abierto.</span><span class="sxs-lookup"><span data-stu-id="29fd6-115">Overwrites the file with the data from the currently open <strong>Stream</strong> object, if the file specified by the <em>Filename</em> parameter already exists.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="29fd6-116">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="29fd6-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="29fd6-117">Estas constantes no tienen equivalentes ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="29fd6-117">These constants do not have ADO/WFC equivalents.</span></span>

