---
title: Propiedad QueryDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5321e834f1dd5ed663033cacb530962d7beeb5a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713369"
---
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="4dbbc-102">Propiedad QueryDef.Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="4dbbc-102">QueryDef.Updatable property (DAO)</span></span>


<span data-ttu-id="4dbbc-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4dbbc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4dbbc-p101">Devuelve un valor que indica si el usuario puede cambiar un objeto DAO. **Boolean** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dbbc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4dbbc-106">Syntax</span></span>

<span data-ttu-id="4dbbc-107">*expresión* . Actualizable</span><span class="sxs-lookup"><span data-stu-id="4dbbc-107">*expression* .Updatable</span></span>

<span data-ttu-id="4dbbc-108">*expresión* Variable que representa un objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="4dbbc-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dbbc-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4dbbc-109">Remarks</span></span>

<span data-ttu-id="4dbbc-110">La propiedad **Updatable** de un objeto **QueryDef** está establecida en **True** si se puede actualizar la consulta de definición, incluso si el objeto **[Recordset](recordset-object-dao.md)** resultante no es actualizable.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

