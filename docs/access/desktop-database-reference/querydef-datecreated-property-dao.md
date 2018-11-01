---
title: QueryDef.DateCreated Property (DAO)
TOCTitle: DateCreated Property
ms:assetid: f7585b34-8314-fb9f-daa6-cd1a8ad59d91
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836910(v=office.15)
ms:contentKeyID: 48548763
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d770decd0bf023a9c2ad8699a8aca4686d73491
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875416"
---
# <a name="querydefdatecreated-property-dao"></a><span data-ttu-id="26466-102">QueryDef.DateCreated Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="26466-102">QueryDef.DateCreated Property (DAO)</span></span>


<span data-ttu-id="26466-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="26466-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="26466-p101">Devuelve la fecha y la hora en que se creó un objeto (únicamente áreas de trabajo de Microsoft). **Variant** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="26466-p101">Returns the date and time that an object was created (Microsoft Access workspaces only). Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="26466-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26466-106">Syntax</span></span>

<span data-ttu-id="26466-107">*expresión* . DateCreated</span><span class="sxs-lookup"><span data-stu-id="26466-107">*expression* .DateCreated</span></span>

<span data-ttu-id="26466-108">*expresión* Variable que representa un objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="26466-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="26466-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26466-109">Remarks</span></span>

<span data-ttu-id="26466-p102">**DateCreated** y **LastUpdated** devuelven la fecha y la hora en que se creó o actualizó por última vez el objeto. En un entorno multiusuario, los usuarios deben obtener estos valores directamente del servidor de archivos para evitar discrepancias en los valores de las propiedades DateCreated y LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="26466-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

