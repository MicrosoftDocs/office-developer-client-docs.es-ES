---
title: Propiedad QueryDef.CacheSize (DAO)
TOCTitle: CacheSize Property
ms:assetid: a84d990e-8180-daa3-7640-47d2be8fd28b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821397(v=office.15)
ms:contentKeyID: 48546899
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d826781bd668cff0a61c655e55834512a289c17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301095"
---
# <a name="querydefcachesize-property-dao"></a><span data-ttu-id="f7cd9-102">Propiedad QueryDef.CacheSize (DAO)</span><span class="sxs-lookup"><span data-stu-id="f7cd9-102">QueryDef.CacheSize property (DAO)</span></span>


<span data-ttu-id="f7cd9-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7cd9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f7cd9-104">Establece o devuelve el número de registros recuperados de un origen de datos ODBC que se almacenarán localmente en caché.</span><span class="sxs-lookup"><span data-stu-id="f7cd9-104">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally.</span></span> <span data-ttu-id="f7cd9-105">**Long** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f7cd9-105">Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7cd9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7cd9-106">Syntax</span></span>

<span data-ttu-id="f7cd9-107">*expresión* . CacheSize</span><span class="sxs-lookup"><span data-stu-id="f7cd9-107">*expression* .CacheSize</span></span>

<span data-ttu-id="f7cd9-108">*expression* Variable que representa un objeto **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="f7cd9-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7cd9-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f7cd9-109">Remarks</span></span>

<span data-ttu-id="f7cd9-p102">El valor de la propiedad **CacheSize** debe estar entre 5 y 1200, pero no debe ser mayor que lo que permita la memoria disponible. Un valor típico es 100. El valor 0 desactiva el almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="f7cd9-p102">The value of the **CacheSize** property must be between 5 and 1200, but not greater than available memory will allow. A typical value is 100. A setting of 0 turns off caching.</span></span>

<span data-ttu-id="f7cd9-113">El motor de base de datos de Microsoft Access solicita registros dentro del intervalo de caché en la caché y solicita registros fuera del intervalo de caché en el servidor.</span><span class="sxs-lookup"><span data-stu-id="f7cd9-113">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="f7cd9-114">Los registros recuperados de la caché no reflejan los cambios simultáneos realizados por otros usuarios en el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="f7cd9-114">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>

