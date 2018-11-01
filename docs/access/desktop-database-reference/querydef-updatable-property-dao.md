---
title: QueryDef.Updatable Property (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ad761c2941cb556ce67c9f716247663220f753f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873694"
---
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="2ed29-102">QueryDef.Updatable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="2ed29-102">QueryDef.Updatable Property (DAO)</span></span>


<span data-ttu-id="2ed29-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2ed29-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2ed29-p101">Devuelve un valor que indica si el usuario puede cambiar un objeto DAO. **Boolean** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="2ed29-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ed29-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ed29-106">Syntax</span></span>

<span data-ttu-id="2ed29-107">*expresión* . Actualizable</span><span class="sxs-lookup"><span data-stu-id="2ed29-107">*expression* .Updatable</span></span>

<span data-ttu-id="2ed29-108">*expresión* Variable que representa un objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="2ed29-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ed29-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ed29-109">Remarks</span></span>

<span data-ttu-id="2ed29-110">La propiedad **Updatable** de un objeto **QueryDef** está establecida en **True** si se puede actualizar la consulta de definición, incluso si el objeto **[Recordset](recordset-object-dao.md)** resultante no es actualizable.</span><span class="sxs-lookup"><span data-stu-id="2ed29-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

