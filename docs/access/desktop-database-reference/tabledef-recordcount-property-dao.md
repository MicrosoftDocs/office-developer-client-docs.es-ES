---
title: Propiedad TableDef. RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5eb9588927c9e35fea54964f16150735a7374cd5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314290"
---
# <a name="tabledefrecordcount-property-dao"></a><span data-ttu-id="e76e6-102">Propiedad TableDef. RecordCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="e76e6-102">TableDef.RecordCount property (DAO)</span></span>


<span data-ttu-id="e76e6-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e76e6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e76e6-104">Devuelve el número total de registros de un objeto **[TableDef](tabledef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="e76e6-104">Returns the total number of records in a **[TableDef](tabledef-object-dao.md)** object.</span></span> <span data-ttu-id="e76e6-105">**Long** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e76e6-105">Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e76e6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e76e6-106">Syntax</span></span>

<span data-ttu-id="e76e6-107">*expresión* . RecordCount</span><span class="sxs-lookup"><span data-stu-id="e76e6-107">*expression* .RecordCount</span></span>

<span data-ttu-id="e76e6-108">*expresión* Variable que representa un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="e76e6-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e76e6-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e76e6-109">Remarks</span></span>

<span data-ttu-id="e76e6-110">Un objeto **Recordset** o **TableDef** sin registros tiene un valor 0 para la propiedad **RecordCount**.</span><span class="sxs-lookup"><span data-stu-id="e76e6-110">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="e76e6-111">Cuando trabaja con objetos vinculados**TableDef**, el valor de la propiedad **RecordCount** siempre es –1.</span><span class="sxs-lookup"><span data-stu-id="e76e6-111">When you work with linked**TableDef** objects, the **RecordCount** property setting is always –1.</span></span>

