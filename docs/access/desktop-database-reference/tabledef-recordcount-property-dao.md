---
title: Propiedad TableDef.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4b24aaa5aec9b17adc169c67733a19a9077a4930
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920924"
---
# <a name="tabledefrecordcount-property-dao"></a><span data-ttu-id="968eb-102">Propiedad TableDef.RecordCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="968eb-102">TableDef.RecordCount property (DAO)</span></span>


<span data-ttu-id="968eb-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="968eb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="968eb-p101">Devuelve el número total de registros de un objeto **[TableDef](tabledef-object-dao.md)**. **Long** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="968eb-p101">Returns the total number of records in a **[TableDef](tabledef-object-dao.md)** object. Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="968eb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="968eb-106">Syntax</span></span>

<span data-ttu-id="968eb-107">*expresión* . RecordCount</span><span class="sxs-lookup"><span data-stu-id="968eb-107">*expression* .RecordCount</span></span>

<span data-ttu-id="968eb-108">*expresión* Variable que representa un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="968eb-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="968eb-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="968eb-109">Remarks</span></span>

<span data-ttu-id="968eb-110">El valor de la propiedad **RecordCount** de un objeto **Recordset** o **TableDef** sin registros es 0.</span><span class="sxs-lookup"><span data-stu-id="968eb-110">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="968eb-111">Cuando trabaja con objetos vinculados**TableDef**, el valor de la propiedad **RecordCount** siempre es –1.</span><span class="sxs-lookup"><span data-stu-id="968eb-111">When you work with linked**TableDef** objects, the **RecordCount** property setting is always –1.</span></span>

