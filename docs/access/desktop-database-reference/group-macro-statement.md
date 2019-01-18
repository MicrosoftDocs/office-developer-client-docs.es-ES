---
title: Grupo (instrucción de macro)
TOCTitle: Group macro statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2dc25621a49d8fd23078a926d6ec6c5de54e54d9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713999"
---
# <a name="group-macro-statement"></a><span data-ttu-id="d358a-102">Grupo (instrucción de macro)</span><span class="sxs-lookup"><span data-stu-id="d358a-102">Group macro statement</span></span>


<span data-ttu-id="d358a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d358a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d358a-104">La instrucción **grupo** permite especificar un bloque de acciones dentro de una macro que se puede expandir o contraer.</span><span class="sxs-lookup"><span data-stu-id="d358a-104">The **Group** statement enables you to specify a block of actions within a macro that you can expand or collapse.</span></span>

## <a name="setting"></a><span data-ttu-id="d358a-105">Valores</span><span class="sxs-lookup"><span data-stu-id="d358a-105">Setting</span></span>

<span data-ttu-id="d358a-106">La acción **Grupo** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="d358a-106">The **Group** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d358a-107">Argumento</span><span class="sxs-lookup"><span data-stu-id="d358a-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="d358a-108">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d358a-108">Required</span></span></p></th>
<th><p><span data-ttu-id="d358a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d358a-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d358a-110"><strong>Descripción</strong></span><span class="sxs-lookup"><span data-stu-id="d358a-110"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="d358a-111">No</span><span class="sxs-lookup"><span data-stu-id="d358a-111">No</span></span></p></td>
<td><p><span data-ttu-id="d358a-112">Una cadena que aparece como el título de un grupo cuando está contraída.</span><span class="sxs-lookup"><span data-stu-id="d358a-112">A string that appears as the title of a group when it is collapsed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d358a-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d358a-113">Remarks</span></span>

<span data-ttu-id="d358a-p101">La instrucción **Grupo** no define una región de una macro que se puede ejecutar por separado. Utilice la instrucción **[Submacro](submacro-macro-statement.md)** para definir un conjunto de acciones que se va a ejecutar por separado en la ventana **Diseñador de macros**.</span><span class="sxs-lookup"><span data-stu-id="d358a-p101">The **Group** statment does not define a region of a macro that can be executed separately. Use the **[Submacro](submacro-macro-statement.md)** statment to define a set of actions to be executed separately in the **Macro Designer** window.</span></span>

