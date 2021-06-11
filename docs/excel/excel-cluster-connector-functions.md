---
title: Excel Funciones del conector de clúster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 41a5cf1ecb7c8f38f4aa5b62a493b3f45c2fe090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408589"
---
# <a name="excel-cluster-connector-functions"></a><span data-ttu-id="9da17-103">Excel Funciones del conector de clúster</span><span class="sxs-lookup"><span data-stu-id="9da17-103">Excel Cluster Connector Functions</span></span>

 <span data-ttu-id="9da17-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9da17-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9da17-105">Microsoft Excel 2013 dll del conector de clúster deben implementar las funciones descritas en esta sección.</span><span class="sxs-lookup"><span data-stu-id="9da17-105">Microsoft Excel 2013 cluster connector DLLs must implement the functions described in this section.</span></span>
  
<span data-ttu-id="9da17-106">Los valores devueltos mencionados en los temas de referencia de esta sección se definen en el archivo de incluye sdk, xlcall.h.</span><span class="sxs-lookup"><span data-stu-id="9da17-106">The return values mentioned in reference topics in this section are defined in the SDK include file, xlcall.h.</span></span>
  
## <a name="cluster-connector-architecture"></a><span data-ttu-id="9da17-107">Arquitectura del conector de clúster</span><span class="sxs-lookup"><span data-stu-id="9da17-107">Cluster Connector Architecture</span></span>

<span data-ttu-id="9da17-108">Excel llamadas a puntos de entrada en un conector de clúster para transferir llamadas de función definidas por el usuario a un clúster de cálculo de alto rendimiento y para la administración de sesiones de clúster.</span><span class="sxs-lookup"><span data-stu-id="9da17-108">Excel calls entry points in a cluster connector to transfer user-defined function calls to a high-performance compute cluster, and for cluster session management.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="9da17-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="9da17-109">In this section</span></span>

[<span data-ttu-id="9da17-110">CallUDF</span><span class="sxs-lookup"><span data-stu-id="9da17-110">CallUDF</span></span>](calludf.md)
  
[<span data-ttu-id="9da17-111">CancelOutstandingRequests</span><span class="sxs-lookup"><span data-stu-id="9da17-111">CancelOutstandingRequests</span></span>](canceloutstandingrequests.md)
  
[<span data-ttu-id="9da17-112">CloseSession</span><span class="sxs-lookup"><span data-stu-id="9da17-112">CloseSession</span></span>](closesession.md)
  
[<span data-ttu-id="9da17-113">OpenSession</span><span class="sxs-lookup"><span data-stu-id="9da17-113">OpenSession</span></span>](opensession.md)
  
[<span data-ttu-id="9da17-114">PingSession</span><span class="sxs-lookup"><span data-stu-id="9da17-114">PingSession</span></span>](pingsession.md)
  
[<span data-ttu-id="9da17-115">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="9da17-115">ShowOptions</span></span>](showoptions.md)
  
## <a name="see-also"></a><span data-ttu-id="9da17-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="9da17-116">See also</span></span>



[<span data-ttu-id="9da17-117">Desarrollar conectores clúster de Excel</span><span class="sxs-lookup"><span data-stu-id="9da17-117">Developing Excel Cluster Connectors</span></span>](developing-excel-cluster-connectors.md)
  
[<span data-ttu-id="9da17-118">Funciones seguras para clústeres</span><span class="sxs-lookup"><span data-stu-id="9da17-118">Cluster Safe Functions</span></span>](cluster-safe-functions.md)

