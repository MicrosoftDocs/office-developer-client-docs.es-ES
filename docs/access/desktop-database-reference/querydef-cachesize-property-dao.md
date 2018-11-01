---
title: QueryDef.CacheSize Property (DAO)
TOCTitle: CacheSize Property
ms:assetid: a84d990e-8180-daa3-7640-47d2be8fd28b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821397(v=office.15)
ms:contentKeyID: 48546899
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 827e0c751101ca68246278c04a408731b77c36a7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885125"
---
# <a name="querydefcachesize-property-dao"></a><span data-ttu-id="6ed83-102">QueryDef.CacheSize Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="6ed83-102">QueryDef.CacheSize Property (DAO)</span></span>


<span data-ttu-id="6ed83-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6ed83-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6ed83-p101">Establece o devuelve el número de registros recuperados de un origen de datos ODBC que se almacenarán localmente en caché. **Long** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="6ed83-p101">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally. Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ed83-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ed83-106">Syntax</span></span>

<span data-ttu-id="6ed83-107">*expresión* . CacheSize</span><span class="sxs-lookup"><span data-stu-id="6ed83-107">*expression* .CacheSize</span></span>

<span data-ttu-id="6ed83-108">*expresión* Variable que representa un objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="6ed83-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ed83-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ed83-109">Remarks</span></span>

<span data-ttu-id="6ed83-p102">El valor de la propiedad **CacheSize** debe estar entre 5 y 1200, pero no debe ser mayor que lo que permita la memoria disponible. Un valor típico es 100. El valor 0 desactiva el almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="6ed83-p102">The value of the **CacheSize** property must be between 5 and 1200, but not greater than available memory will allow. A typical value is 100. A setting of 0 turns off caching.</span></span>

<span data-ttu-id="6ed83-113">El motor de base de datos de Microsoft Access solicita registros dentro del intervalo de caché en la caché y solicita registros fuera del intervalo de caché en el servidor.</span><span class="sxs-lookup"><span data-stu-id="6ed83-113">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="6ed83-114">Los registros recuperados de la caché no reflejan los cambios simultáneos realizados por otros usuarios en el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="6ed83-114">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>

