---
title: Propiedad QueryDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b0c1a85029270641a944d822ee81954ca1f2528e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919811"
---
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="e084e-102">Propiedad QueryDef.Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="e084e-102">QueryDef.Updatable property (DAO)</span></span>


<span data-ttu-id="e084e-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e084e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e084e-p101">Devuelve un valor que indica si el usuario puede cambiar un objeto DAO. **Boolean** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="e084e-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e084e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e084e-106">Syntax</span></span>

<span data-ttu-id="e084e-107">*expresión* . Actualizable</span><span class="sxs-lookup"><span data-stu-id="e084e-107">*expression* .Updatable</span></span>

<span data-ttu-id="e084e-108">*expresión* Variable que representa un objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="e084e-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e084e-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e084e-109">Remarks</span></span>

<span data-ttu-id="e084e-110">La propiedad **Updatable** de un objeto **QueryDef** está establecida en **True** si se puede actualizar la consulta de definición, incluso si el objeto **[Recordset](recordset-object-dao.md)** resultante no es actualizable.</span><span class="sxs-lookup"><span data-stu-id="e084e-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

