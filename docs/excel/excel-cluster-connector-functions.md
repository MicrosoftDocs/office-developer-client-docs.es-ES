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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408589"
---
# <a name="excel-cluster-connector-functions"></a><span data-ttu-id="6b308-103">Funciones del conector de clúster de Excel</span><span class="sxs-lookup"><span data-stu-id="6b308-103">Excel Cluster Connector Functions</span></span>

 <span data-ttu-id="6b308-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6b308-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6b308-105">Los archivos DLL del conector de clúster de Microsoft Excel 2013 deben implementar las funciones descritas en esta sección.</span><span class="sxs-lookup"><span data-stu-id="6b308-105">Microsoft Excel 2013 cluster connector DLLs must implement the functions described in this section.</span></span>
  
<span data-ttu-id="6b308-106">Los valores devueltos que se mencionan en los temas de referencia de esta sección se definen en el archivo de inclusión del SDK, xlcall. h.</span><span class="sxs-lookup"><span data-stu-id="6b308-106">The return values mentioned in reference topics in this section are defined in the SDK include file, xlcall.h.</span></span>
  
## <a name="cluster-connector-architecture"></a><span data-ttu-id="6b308-107">Arquitectura del conector de clúster</span><span class="sxs-lookup"><span data-stu-id="6b308-107">Cluster Connector Architecture</span></span>

<span data-ttu-id="6b308-108">Excel llama a puntos de entrada en un conector de clúster para transferir llamadas de función definidas por el usuario a un clúster de cómputo de alto rendimiento y para la administración de sesiones de clúster.</span><span class="sxs-lookup"><span data-stu-id="6b308-108">Excel calls entry points in a cluster connector to transfer user-defined function calls to a high-performance compute cluster, and for cluster session management.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="6b308-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="6b308-109">In this section</span></span>

[<span data-ttu-id="6b308-110">CallUDF</span><span class="sxs-lookup"><span data-stu-id="6b308-110">CallUDF</span></span>](calludf.md)
  
[<span data-ttu-id="6b308-111">CancelOutstandingRequests</span><span class="sxs-lookup"><span data-stu-id="6b308-111">CancelOutstandingRequests</span></span>](canceloutstandingrequests.md)
  
[<span data-ttu-id="6b308-112">CloseSession</span><span class="sxs-lookup"><span data-stu-id="6b308-112">CloseSession</span></span>](closesession.md)
  
[<span data-ttu-id="6b308-113">OpenSession</span><span class="sxs-lookup"><span data-stu-id="6b308-113">OpenSession</span></span>](opensession.md)
  
[<span data-ttu-id="6b308-114">PingSession</span><span class="sxs-lookup"><span data-stu-id="6b308-114">PingSession</span></span>](pingsession.md)
  
[<span data-ttu-id="6b308-115">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="6b308-115">ShowOptions</span></span>](showoptions.md)
  
## <a name="see-also"></a><span data-ttu-id="6b308-116">Ver también</span><span class="sxs-lookup"><span data-stu-id="6b308-116">See also</span></span>



[<span data-ttu-id="6b308-117">Desarrollar conectores clúster de Excel</span><span class="sxs-lookup"><span data-stu-id="6b308-117">Developing Excel Cluster Connectors</span></span>](developing-excel-cluster-connectors.md)
  
[<span data-ttu-id="6b308-118">Funciones seguras para clústeres</span><span class="sxs-lookup"><span data-stu-id="6b308-118">Cluster Safe Functions</span></span>](cluster-safe-functions.md)

