---
title: Propiedad QueryDef. LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 3b7818d4-054e-54e2-bf63-58b340bb4a90
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192665(v=office.15)
ms:contentKeyID: 48544287
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1876e92381828075edca3bbfcbae63e706a21365
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303314"
---
# <a name="querydeflastupdated-property-dao"></a><span data-ttu-id="e1bce-102">Propiedad QueryDef. LastUpdated (DAO)</span><span class="sxs-lookup"><span data-stu-id="e1bce-102">QueryDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="e1bce-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e1bce-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e1bce-104">Devuelve la fecha y la hora del último cambio realizado en un objeto.</span><span class="sxs-lookup"><span data-stu-id="e1bce-104">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="e1bce-105">**Variant** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="e1bce-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1bce-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1bce-106">Syntax</span></span>

<span data-ttu-id="e1bce-107">*expresión* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="e1bce-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="e1bce-108">*expresión* Variable que representa un objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="e1bce-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1bce-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e1bce-109">Remarks</span></span>

<span data-ttu-id="e1bce-p102">**DateCreated** y **LastUpdated** devuelven la fecha y la hora en la que un objeto se creó o se actualizó por última vez. En un entorno multiusuario, los usuarios deben obtener estos valores directamente desde el servidor de archivos para evitar discrepancias con los valores de las propiedades DateCreated y LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="e1bce-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

