---
title: TableDef.LastUpdated Property (DAO)
TOCTitle: LastUpdated Property
ms:assetid: fafe54e2-2cf0-5874-92b9-6e20a65e77ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837164(v=office.15)
ms:contentKeyID: 48548859
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10d0203bd30c2e03f7cd2aaa761ac1cf76b12f94
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870866"
---
# <a name="tabledeflastupdated-property-dao"></a><span data-ttu-id="a7045-102">TableDef.LastUpdated Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="a7045-102">TableDef.LastUpdated Property (DAO)</span></span>


<span data-ttu-id="a7045-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a7045-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a7045-p101">Devuelve la fecha y la hora del último cambio efectuado en un objeto. **Variant** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="a7045-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7045-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7045-106">Syntax</span></span>

<span data-ttu-id="a7045-107">*expresión* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="a7045-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="a7045-108">*expresión* Variable que representa un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="a7045-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7045-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7045-109">Remarks</span></span>

<span data-ttu-id="a7045-p102">**DateCreated** y **LastUpdated** devuelven la fecha y la hora en que se creó o actualizó por última vez el objeto. En un entorno multiusuario, los usuarios deben obtener estos valores directamente del servidor de archivos para evitar discrepancias en los valores de las propiedades DateCreated y LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="a7045-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

