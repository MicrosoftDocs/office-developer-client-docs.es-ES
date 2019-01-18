---
title: Propiedad TableDef.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5eb9588927c9e35fea54964f16150735a7374cd5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722868"
---
# <a name="tabledefrecordcount-property-dao"></a><span data-ttu-id="63fea-102">Propiedad TableDef.RecordCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="63fea-102">TableDef.RecordCount property (DAO)</span></span>


<span data-ttu-id="63fea-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="63fea-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="63fea-p101">Devuelve el número total de registros de un objeto **[TableDef](tabledef-object-dao.md)**. **Long** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="63fea-p101">Returns the total number of records in a **[TableDef](tabledef-object-dao.md)** object. Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="63fea-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63fea-106">Syntax</span></span>

<span data-ttu-id="63fea-107">*expresión* . RecordCount</span><span class="sxs-lookup"><span data-stu-id="63fea-107">*expression* .RecordCount</span></span>

<span data-ttu-id="63fea-108">*expresión* Variable que representa un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="63fea-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="63fea-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63fea-109">Remarks</span></span>

<span data-ttu-id="63fea-110">El valor de la propiedad **RecordCount** de un objeto **Recordset** o **TableDef** sin registros es 0.</span><span class="sxs-lookup"><span data-stu-id="63fea-110">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="63fea-111">Cuando trabaja con objetos vinculados**TableDef**, el valor de la propiedad **RecordCount** siempre es –1.</span><span class="sxs-lookup"><span data-stu-id="63fea-111">When you work with linked**TableDef** objects, the **RecordCount** property setting is always –1.</span></span>

