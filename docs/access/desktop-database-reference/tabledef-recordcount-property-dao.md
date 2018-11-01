---
title: TableDef.RecordCount Property (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7ef77f5882f4b215764a82d343d59f1f31487e58
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886119"
---
# <a name="tabledefrecordcount-property-dao"></a><span data-ttu-id="626c6-102">TableDef.RecordCount Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="626c6-102">TableDef.RecordCount Property (DAO)</span></span>


<span data-ttu-id="626c6-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="626c6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="626c6-p101">Devuelve el número total de registros de un objeto **[TableDef](tabledef-object-dao.md)**. **Long** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="626c6-p101">Returns the total number of records in a **[TableDef](tabledef-object-dao.md)** object. Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="626c6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="626c6-106">Syntax</span></span>

<span data-ttu-id="626c6-107">*expresión* . RecordCount</span><span class="sxs-lookup"><span data-stu-id="626c6-107">*expression* .RecordCount</span></span>

<span data-ttu-id="626c6-108">*expresión* Variable que representa un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="626c6-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="626c6-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="626c6-109">Remarks</span></span>

<span data-ttu-id="626c6-110">El valor de la propiedad **RecordCount** de un objeto **Recordset** o **TableDef** sin registros es 0.</span><span class="sxs-lookup"><span data-stu-id="626c6-110">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="626c6-111">Cuando trabaja con objetos vinculados**TableDef**, el valor de la propiedad **RecordCount** siempre es –1.</span><span class="sxs-lookup"><span data-stu-id="626c6-111">When you work with linked**TableDef** objects, the **RecordCount** property setting is always –1.</span></span>

