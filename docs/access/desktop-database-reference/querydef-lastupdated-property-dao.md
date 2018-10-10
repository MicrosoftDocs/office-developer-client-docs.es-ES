---
title: QueryDef.LastUpdated Property (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 3b7818d4-054e-54e2-bf63-58b340bb4a90
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192665(v=office.15)
ms:contentKeyID: 48544287
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 37a95cefb5af5070470fb5973076e230d76c3d98
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486728"
---
# <a name="querydeflastupdated-property-dao"></a><span data-ttu-id="86fed-102">QueryDef.LastUpdated Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="86fed-102">QueryDef.LastUpdated Property (DAO)</span></span>


<span data-ttu-id="86fed-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="86fed-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="86fed-p101">Devuelve la fecha y la hora del último cambio efectuado en un objeto. **Variant** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="86fed-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="86fed-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86fed-106">Syntax</span></span>

<span data-ttu-id="86fed-107">*expresión* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="86fed-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="86fed-108">*expresión* Variable que representa un objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="86fed-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="86fed-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86fed-109">Remarks</span></span>

<span data-ttu-id="86fed-p102">**DateCreated** y **LastUpdated** devuelven la fecha y la hora en que se creó o actualizó por última vez el objeto. En un entorno multiusuario, los usuarios deben obtener estos valores directamente del servidor de archivos para evitar discrepancias en los valores de las propiedades DateCreated y LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="86fed-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

