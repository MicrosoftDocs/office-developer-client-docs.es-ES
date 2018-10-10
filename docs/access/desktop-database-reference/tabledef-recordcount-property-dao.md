---
title: TableDef.RecordCount Property (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b1d1ab4fee16a9664733c71522cb07a49dde149
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485123"
---
# <a name="tabledefrecordcount-property-dao"></a><span data-ttu-id="98678-102">TableDef.RecordCount Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="98678-102">TableDef.RecordCount Property (DAO)</span></span>


<span data-ttu-id="98678-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="98678-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="98678-p101">Devuelve el número total de registros de un objeto **[TableDef](tabledef-object-dao.md)**. **Long** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="98678-p101">Returns the total number of records in a **[TableDef](tabledef-object-dao.md)** object. Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="98678-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98678-106">Syntax</span></span>

<span data-ttu-id="98678-107">*expresión* . RecordCount</span><span class="sxs-lookup"><span data-stu-id="98678-107">*expression* .RecordCount</span></span>

<span data-ttu-id="98678-108">*expresión* Variable que representa un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="98678-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="98678-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98678-109">Remarks</span></span>

<span data-ttu-id="98678-110">El valor de la propiedad **RecordCount** de un objeto **Recordset** o **TableDef** sin registros es 0.</span><span class="sxs-lookup"><span data-stu-id="98678-110">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="98678-111">Cuando trabaja con objetos vinculados**TableDef**, el valor de la propiedad **RecordCount** siempre es –1.</span><span class="sxs-lookup"><span data-stu-id="98678-111">When you work with linked**TableDef** objects, the **RecordCount** property setting is always –1.</span></span>

