---
title: Propiedad QueryDef.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 3b7818d4-054e-54e2-bf63-58b340bb4a90
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192665(v=office.15)
ms:contentKeyID: 48544287
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 98bb600e6f3f1c9587eca110269e8b6b3765e40f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921276"
---
# <a name="querydeflastupdated-property-dao"></a><span data-ttu-id="86440-102">Propiedad QueryDef.LastUpdated (DAO)</span><span class="sxs-lookup"><span data-stu-id="86440-102">QueryDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="86440-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="86440-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="86440-p101">Devuelve la fecha y la hora del último cambio efectuado en un objeto. **Variant** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="86440-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="86440-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86440-106">Syntax</span></span>

<span data-ttu-id="86440-107">*expresión* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="86440-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="86440-108">*expresión* Variable que representa un objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="86440-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="86440-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86440-109">Remarks</span></span>

<span data-ttu-id="86440-p102">**DateCreated** y **LastUpdated** devuelven la fecha y la hora en que se creó o actualizó por última vez el objeto. En un entorno multiusuario, los usuarios deben obtener estos valores directamente del servidor de archivos para evitar discrepancias en los valores de las propiedades DateCreated y LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="86440-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

