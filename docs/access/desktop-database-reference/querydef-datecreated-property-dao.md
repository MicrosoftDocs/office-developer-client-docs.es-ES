---
title: Propiedad QueryDef.DateCreated (DAO)
TOCTitle: DateCreated Property
ms:assetid: f7585b34-8314-fb9f-daa6-cd1a8ad59d91
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836910(v=office.15)
ms:contentKeyID: 48548763
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4a120eed6c20db73e1c23f31ea9329d00da2f0d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301074"
---
# <a name="querydefdatecreated-property-dao"></a><span data-ttu-id="8fdeb-102">Propiedad QueryDef.DateCreated (DAO)</span><span class="sxs-lookup"><span data-stu-id="8fdeb-102">QueryDef.DateCreated property (DAO)</span></span>


<span data-ttu-id="8fdeb-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8fdeb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8fdeb-104">Devuelve la fecha y la hora en la que se creó un objeto (sólo para áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="8fdeb-104">Returns the date and time that an object was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="8fdeb-105">**Variant** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="8fdeb-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fdeb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8fdeb-106">Syntax</span></span>

<span data-ttu-id="8fdeb-107">*expresión* . DateCreated</span><span class="sxs-lookup"><span data-stu-id="8fdeb-107">*expression* .DateCreated</span></span>

<span data-ttu-id="8fdeb-108">*expression* Variable que representa un objeto **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="8fdeb-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fdeb-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8fdeb-109">Remarks</span></span>

<span data-ttu-id="8fdeb-p102">**DateCreated** y **LastUpdated** devuelven la fecha y la hora en la que un objeto se creó o se actualizó por última vez. En un entorno multiusuario, los usuarios deben obtener estos valores directamente desde el servidor de archivos para evitar discrepancias con los valores de las propiedades DateCreated y LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="8fdeb-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

