---
title: Grupo (instrucción de macro)
TOCTitle: Group Macro Statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 189744d228db0dadd3260ce77457daf8724828f8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484818"
---
# <a name="group-macro-statement"></a><span data-ttu-id="0e640-102">Grupo (instrucción de macro)</span><span class="sxs-lookup"><span data-stu-id="0e640-102">Group Macro Statement</span></span>


<span data-ttu-id="0e640-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e640-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0e640-104">La instrucción **grupo** permite especificar un bloque de acciones dentro de una macro que se puede expandir o contraer.</span><span class="sxs-lookup"><span data-stu-id="0e640-104">The **Group** statement enables you to specify a block of actions within a macro that you can expand or collapse.</span></span>

## <a name="setting"></a><span data-ttu-id="0e640-105">Valores</span><span class="sxs-lookup"><span data-stu-id="0e640-105">Setting</span></span>

<span data-ttu-id="0e640-106">La acción **Grupo** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="0e640-106">The **Group** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e640-107">Argumento</span><span class="sxs-lookup"><span data-stu-id="0e640-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="0e640-108">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="0e640-108">Required</span></span></p></th>
<th><p><span data-ttu-id="0e640-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e640-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e640-110"><strong>Descripción</strong></span><span class="sxs-lookup"><span data-stu-id="0e640-110"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="0e640-111">No</span><span class="sxs-lookup"><span data-stu-id="0e640-111">No</span></span></p></td>
<td><p><span data-ttu-id="0e640-112">Una cadena que aparece como el título de un grupo cuando está contraída.</span><span class="sxs-lookup"><span data-stu-id="0e640-112">A string that appears as the title of a group when it is collapsed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0e640-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0e640-113">Remarks</span></span>

<span data-ttu-id="0e640-p101">La instrucción **Grupo** no define una región de una macro que se puede ejecutar por separado. Utilice la instrucción **[Submacro](submacro-macro-statement.md)** para definir un conjunto de acciones que se va a ejecutar por separado en la ventana **Diseñador de macros**.</span><span class="sxs-lookup"><span data-stu-id="0e640-p101">The **Group** statment does not define a region of a macro that can be executed separately. Use the **[Submacro](submacro-macro-statement.md)** statment to define a set of actions to be executed separately in the **Macro Designer** window.</span></span>

