---
title: QueryDef.DateCreated Property (DAO)
TOCTitle: DateCreated Property
ms:assetid: f7585b34-8314-fb9f-daa6-cd1a8ad59d91
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836910(v=office.15)
ms:contentKeyID: 48548763
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62fcad68a50ac7f2a09675d9ac51734c4147d207
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486281"
---
# <a name="querydefdatecreated-property-dao"></a><span data-ttu-id="786fe-102">QueryDef.DateCreated Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="786fe-102">QueryDef.DateCreated Property (DAO)</span></span>


<span data-ttu-id="786fe-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="786fe-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="786fe-p101">Devuelve la fecha y la hora en que se creó un objeto (únicamente áreas de trabajo de Microsoft). **Variant** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="786fe-p101">Returns the date and time that an object was created (Microsoft Access workspaces only). Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="786fe-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="786fe-106">Syntax</span></span>

<span data-ttu-id="786fe-107">*expresión* . DateCreated</span><span class="sxs-lookup"><span data-stu-id="786fe-107">*expression* .DateCreated</span></span>

<span data-ttu-id="786fe-108">*expresión* Variable que representa un objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="786fe-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="786fe-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="786fe-109">Remarks</span></span>

<span data-ttu-id="786fe-p102">**DateCreated** y **LastUpdated** devuelven la fecha y la hora en que se creó o actualizó por última vez el objeto. En un entorno multiusuario, los usuarios deben obtener estos valores directamente del servidor de archivos para evitar discrepancias en los valores de las propiedades DateCreated y LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="786fe-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

