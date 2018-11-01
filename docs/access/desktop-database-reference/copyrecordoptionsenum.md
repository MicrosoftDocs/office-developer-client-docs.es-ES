---
title: CopyRecordOptionsEnum
TOCTitle: CopyRecordOptionsEnum
ms:assetid: ab9426e9-0e4e-6c85-43cf-e4a205a7c4c0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249795(v=office.15)
ms:contentKeyID: 48546975
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d3c3ddd8174a646bccd37cec758e85e17f4cdaec
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882780"
---
# <a name="copyrecordoptionsenum"></a><span data-ttu-id="c610c-102">CopyRecordOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="c610c-102">CopyRecordOptionsEnum</span></span>


<span data-ttu-id="c610c-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c610c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c610c-104">Especifica el comportamiento del método [CopyRecord](copyrecord-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c610c-104">Specifies the behavior of the [CopyRecord](copyrecord-method-ado.md) method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c610c-105">Constante</span><span class="sxs-lookup"><span data-stu-id="c610c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="c610c-106">Valor</span><span class="sxs-lookup"><span data-stu-id="c610c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c610c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c610c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c610c-108"><strong>adCopyAllowEmulation</strong></span><span class="sxs-lookup"><span data-stu-id="c610c-108"><strong>adCopyAllowEmulation</strong></span></span></p></td>
<td><p><span data-ttu-id="c610c-109">4</span><span class="sxs-lookup"><span data-stu-id="c610c-109">4</span></span></p></td>
<td><p><span data-ttu-id="c610c-p101">Indica que el proveedor <em>Origen</em> intenta simular la copia mediante operaciones de descarga y carga si este método falla debido a que <em>Destino</em> está en un servidor diferente o es atendido por un proveedor diferente de <em>Origen</em>. Tenga en cuenta que las capacidades diferentes de los proveedores pueden dificultar el rendimiento u ocasionar la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="c610c-p101">Indicates that the <em>Source</em> provider attempts to simulate the copy using download and upload operations if this method fails due to <em>Destination</em> being on a different server or is serviced by a different provider than <em>Source</em>. Note that differing provider capabilities may hamper performance or lose data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c610c-112"><strong>adCopyNonRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="c610c-112"><strong>adCopyNonRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="c610c-113">2</span><span class="sxs-lookup"><span data-stu-id="c610c-113">2</span></span></p></td>
<td><p><span data-ttu-id="c610c-p102">Copia el directorio actual, pero ninguno de sus subdirectorios, en el destino. La operación de copia no es recursiva.</span><span class="sxs-lookup"><span data-stu-id="c610c-p102">Copies the current directory, but none of its subdirectories, to the destination. The copy operation is not recursive.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c610c-116"><strong>adCopyOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="c610c-116"><strong>adCopyOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="c610c-117">1</span><span class="sxs-lookup"><span data-stu-id="c610c-117">1</span></span></p></td>
<td><p><span data-ttu-id="c610c-118">Sobrescribe el archivo o el directorio si el <em>Destino</em> apunta a un archivo o directorio existentes.</span><span class="sxs-lookup"><span data-stu-id="c610c-118">Overwrites the file or directory if the <em>Destination</em> points to an existing file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c610c-119"><strong>Como</strong></span><span class="sxs-lookup"><span data-stu-id="c610c-119"><strong>adCopyUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="c610c-120">-1</span><span class="sxs-lookup"><span data-stu-id="c610c-120">-1</span></span></p></td>
<td><p><span data-ttu-id="c610c-p103">Valor predeterminado. Realiza la operación de copia predeterminada: la operación falla si el archivo o el directorio de destino ya existen, y la operación copia de forma recursiva.</span><span class="sxs-lookup"><span data-stu-id="c610c-p103">Default. Performs the default copy operation: The operation fails if the destination file or directory already exists, and the operation copies recursively.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="c610c-123">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="c610c-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="c610c-124">Estas constantes no tienen equivalentes ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="c610c-124">These constants do not have ADO/WFC equivalents.</span></span>

