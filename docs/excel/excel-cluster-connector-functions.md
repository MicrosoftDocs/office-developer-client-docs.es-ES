---
title: Funciones del conector de clúster de Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 41a5cf1ecb7c8f38f4aa5b62a493b3f45c2fe090
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311070"
---
# <a name="excel-cluster-connector-functions"></a><span data-ttu-id="7ead7-103">Funciones del conector de clúster de Excel</span><span class="sxs-lookup"><span data-stu-id="7ead7-103">Excel Cluster Connector Functions</span></span>

 <span data-ttu-id="7ead7-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7ead7-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7ead7-105">Los archivos DLL del conector de clúster de Microsoft Excel 2013 deben implementar las funciones descritas en esta sección.</span><span class="sxs-lookup"><span data-stu-id="7ead7-105">Microsoft Excel 2013 cluster connector DLLs must implement the functions described in this section.</span></span>
  
<span data-ttu-id="7ead7-106">Los valores devueltos que se mencionan en los temas de referencia de esta sección se definen en el archivo de inclusión del SDK, xlcall. h.</span><span class="sxs-lookup"><span data-stu-id="7ead7-106">The return values mentioned in reference topics in this section are defined in the SDK include file, xlcall.h.</span></span>
  
## <a name="cluster-connector-architecture"></a><span data-ttu-id="7ead7-107">Arquitectura del conector de clúster</span><span class="sxs-lookup"><span data-stu-id="7ead7-107">Cluster Connector Architecture</span></span>

<span data-ttu-id="7ead7-108">Excel llama a puntos de entrada en un conector de clúster para transferir llamadas de función definidas por el usuario a un clúster de cómputo de alto rendimiento y para la administración de sesiones de clúster.</span><span class="sxs-lookup"><span data-stu-id="7ead7-108">Excel calls entry points in a cluster connector to transfer user-defined function calls to a high-performance compute cluster, and for cluster session management.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="7ead7-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="7ead7-109">In this section</span></span>

[<span data-ttu-id="7ead7-110">CallUDF</span><span class="sxs-lookup"><span data-stu-id="7ead7-110">CallUDF</span></span>](calludf.md)
  
[<span data-ttu-id="7ead7-111">CancelOutstandingRequests</span><span class="sxs-lookup"><span data-stu-id="7ead7-111">CancelOutstandingRequests</span></span>](canceloutstandingrequests.md)
  
[<span data-ttu-id="7ead7-112">CloseSession</span><span class="sxs-lookup"><span data-stu-id="7ead7-112">CloseSession</span></span>](closesession.md)
  
[<span data-ttu-id="7ead7-113">OpenSession</span><span class="sxs-lookup"><span data-stu-id="7ead7-113">OpenSession</span></span>](opensession.md)
  
[<span data-ttu-id="7ead7-114">PingSession</span><span class="sxs-lookup"><span data-stu-id="7ead7-114">PingSession</span></span>](pingsession.md)
  
[<span data-ttu-id="7ead7-115">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="7ead7-115">ShowOptions</span></span>](showoptions.md)
  
## <a name="see-also"></a><span data-ttu-id="7ead7-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ead7-116">See also</span></span>



[<span data-ttu-id="7ead7-117">Desarrollar conectores clúster de Excel</span><span class="sxs-lookup"><span data-stu-id="7ead7-117">Developing Excel Cluster Connectors</span></span>](developing-excel-cluster-connectors.md)
  
[<span data-ttu-id="7ead7-118">Funciones seguras para clústeres</span><span class="sxs-lookup"><span data-stu-id="7ead7-118">Cluster Safe Functions</span></span>](cluster-safe-functions.md)

