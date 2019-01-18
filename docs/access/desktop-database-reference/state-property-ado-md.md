---
title: State (propiedad, ADO MD)
TOCTitle: State property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 051a9f0cc50ae3a60edb033f6807f72fc0688976
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702449"
---
# <a name="state-property-ado-md"></a><span data-ttu-id="3c68d-102">State (propiedad, ADO MD)</span><span class="sxs-lookup"><span data-stu-id="3c68d-102">State property (ADO MD)</span></span>


<span data-ttu-id="3c68d-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c68d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3c68d-104">Indica el estado actual del conjunto de celdas.</span><span class="sxs-lookup"><span data-stu-id="3c68d-104">Indicates the current state of the cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="3c68d-105">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="3c68d-105">Return values</span></span>

<span data-ttu-id="3c68d-p101">Devuelve un entero **Long** que indica el estado actual del objeto [Cellset](cellset-object-ado-md.md) y es de sólo lectura. Los valores siguientes son válidos: **adStateClosed** (0) y **adStateOpen** (1).</span><span class="sxs-lookup"><span data-stu-id="3c68d-p101">Returns a **Long** integer indicating the current condition of the [Cellset](cellset-object-ado-md.md) object and is read-only. The following values are valid: **adStateClosed** (0) and **adStateOpen** (1).</span></span>

## <a name="remarks"></a><span data-ttu-id="3c68d-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3c68d-108">Remarks</span></span>

<span data-ttu-id="3c68d-p102">Para usar los nombres de constantes [ObjectStateEnum](objectstateenum.md), debe existir una referencia a la biblioteca de tipos ADO en su proyecto. Vea [Utilizar ADO con ADO MD](using-ado-with-ado-md.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="3c68d-p102">To use the [ObjectStateEnum](objectstateenum.md) constant names, you must have the ADO type library referenced in your project. See [Using ADO with ADO MD](using-ado-with-ado-md.md) for more information.</span></span>

