---
title: Propiedad Document.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: abb766f7a47cbacaededf65eb2b5e9145bf88c60
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698382"
---
# <a name="documentlastupdated-property-dao"></a><span data-ttu-id="04049-102">Propiedad Document.LastUpdated (DAO)</span><span class="sxs-lookup"><span data-stu-id="04049-102">Document.LastUpdated property (DAO)</span></span>


<span data-ttu-id="04049-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="04049-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="04049-p101">Devuelve la fecha y la hora del último cambio efectuado en un objeto. **Variant** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="04049-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="04049-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04049-106">Syntax</span></span>

<span data-ttu-id="04049-107">*expresión* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="04049-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="04049-108">*expresión* Variable que representa un objeto **Document** .</span><span class="sxs-lookup"><span data-stu-id="04049-108">*expression* A variable that represents a **Document** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="04049-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04049-109">Remarks</span></span>

<span data-ttu-id="04049-p102">**DateCreated** y **LastUpdated** devuelven la fecha y la hora en que se creó o actualizó por última vez el objeto. En un entorno multiusuario, los usuarios deben obtener estos valores directamente del servidor de archivos para evitar discrepancias en los valores de las propiedades DateCreated y LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="04049-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

