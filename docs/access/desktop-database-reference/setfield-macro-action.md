---
title: EstablecerCampo (acción de macro)
TOCTitle: SetField macro action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4fbf7252729c7b376da6ebe67f59941c1caf924d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314619"
---
# <a name="setfield-macro-action"></a><span data-ttu-id="3e976-102">EstablecerCampo (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="3e976-102">SetField macro action</span></span>

<span data-ttu-id="3e976-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3e976-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3e976-104">La acción **EstablecerCampo** puede utilizarse para asignar un valor a un campo.</span><span class="sxs-lookup"><span data-stu-id="3e976-104">The **SetField** action can be used to assign a value to a field.</span></span>

> [!NOTE]
> <span data-ttu-id="3e976-105">La acción **EstablecerCampo** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="3e976-105">The **SetField** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="3e976-106">Setting</span><span class="sxs-lookup"><span data-stu-id="3e976-106">Setting</span></span>

<span data-ttu-id="3e976-107">La acción **EstablecerCampo** utiliza los argumentos enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3e976-107">The **SetField** action has the arguments listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3e976-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="3e976-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="3e976-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e976-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e976-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="3e976-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="3e976-111">Una cadena que identifica el campo.</span><span class="sxs-lookup"><span data-stu-id="3e976-111">A string that identifies the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e976-112"><strong>Valor</strong></span><span class="sxs-lookup"><span data-stu-id="3e976-112"><strong>Value</strong></span></span></p></td>
<td><p><span data-ttu-id="3e976-113">Expresión que especifica el valor que se asignará al campo.</span><span class="sxs-lookup"><span data-stu-id="3e976-113">An expression that specifies the value to assign to the field.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3e976-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3e976-114">Remarks</span></span>

<span data-ttu-id="3e976-115">No se puede utilizar la acción **EstablecerCampo** fuera de un bloque de datos **[CrearRegistro](createrecord-data-block.md)** o **[EditarRegistro](editrecord-data-block.md)**.</span><span class="sxs-lookup"><span data-stu-id="3e976-115">The **SetField** action cannot be used outside of an **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block.</span></span>

