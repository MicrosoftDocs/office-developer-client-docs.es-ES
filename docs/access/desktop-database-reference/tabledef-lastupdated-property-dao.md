---
title: Propiedad TableDef.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: fafe54e2-2cf0-5874-92b9-6e20a65e77ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837164(v=office.15)
ms:contentKeyID: 48548859
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 994543132fb5323566bd876da066419d0986bd91
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722777"
---
# <a name="tabledeflastupdated-property-dao"></a><span data-ttu-id="18771-102">Propiedad TableDef.LastUpdated (DAO)</span><span class="sxs-lookup"><span data-stu-id="18771-102">TableDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="18771-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="18771-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="18771-p101">Devuelve la fecha y la hora del último cambio efectuado en un objeto. **Variant** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="18771-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="18771-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18771-106">Syntax</span></span>

<span data-ttu-id="18771-107">*expresión* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="18771-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="18771-108">*expresión* Variable que representa un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="18771-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="18771-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18771-109">Remarks</span></span>

<span data-ttu-id="18771-p102">**DateCreated** y **LastUpdated** devuelven la fecha y la hora en que se creó o actualizó por última vez el objeto. En un entorno multiusuario, los usuarios deben obtener estos valores directamente del servidor de archivos para evitar discrepancias en los valores de las propiedades DateCreated y LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="18771-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

