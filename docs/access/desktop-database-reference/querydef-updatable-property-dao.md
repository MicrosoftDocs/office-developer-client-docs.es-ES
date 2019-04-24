---
title: Propiedad QueryDef. Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5321e834f1dd5ed663033cacb530962d7beeb5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303335"
---
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="66839-102">Propiedad QueryDef. Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="66839-102">QueryDef.Updatable property (DAO)</span></span>


<span data-ttu-id="66839-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="66839-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="66839-104">Devuelve un valor que indica si el usuario puede cambiar un objeto DAO.</span><span class="sxs-lookup"><span data-stu-id="66839-104">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="66839-105">**Boolean** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="66839-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="66839-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66839-106">Syntax</span></span>

<span data-ttu-id="66839-107">*expresión* . Actualizable</span><span class="sxs-lookup"><span data-stu-id="66839-107">*expression* .Updatable</span></span>

<span data-ttu-id="66839-108">*expresión* Variable que representa un objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="66839-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="66839-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="66839-109">Remarks</span></span>

<span data-ttu-id="66839-110">La propiedad **Updatable** de un objeto **QueryDef** está establecida en **True** si se puede actualizar la consulta de definición, incluso si el objeto **[Recordset](recordset-object-dao.md)** resultante no es actualizable.</span><span class="sxs-lookup"><span data-stu-id="66839-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

