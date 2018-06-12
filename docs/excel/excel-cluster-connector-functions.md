---
title: Funciones de conector de clúster de Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4a069aa4ed3ee17320ac65ab793ea8812153cc18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815554"
---
# <a name="excel-cluster-connector-functions"></a><span data-ttu-id="6d77c-103">Funciones de conector de clúster de Excel</span><span class="sxs-lookup"><span data-stu-id="6d77c-103">Excel Cluster Connector Functions</span></span>

 <span data-ttu-id="6d77c-104">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6d77c-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6d77c-105">Conector de clúster de Microsoft Excel 2013 dll debe implementar las funciones que se describen en esta sección.</span><span class="sxs-lookup"><span data-stu-id="6d77c-105">Microsoft Excel 2013 cluster connector DLLs must implement the functions described in this section.</span></span>
  
<span data-ttu-id="6d77c-106">Los valores devueltos que se mencionan en los temas de esta sección se definen en el SDK de referencia incluyen archivo, xlcall.h.</span><span class="sxs-lookup"><span data-stu-id="6d77c-106">The return values mentioned in reference topics in this section are defined in the SDK include file, xlcall.h.</span></span>
  
## <a name="cluster-connector-architecture"></a><span data-ttu-id="6d77c-107">Arquitectura del conector de clúster</span><span class="sxs-lookup"><span data-stu-id="6d77c-107">Cluster Connector Architecture</span></span>

<span data-ttu-id="6d77c-108">Excel llama a puntos de entrada en un conector de clúster para transferir las llamadas de función definida por el usuario a un clúster de cálculo de alto rendimiento y para la administración de sesiones de clúster.</span><span class="sxs-lookup"><span data-stu-id="6d77c-108">Excel calls entry points in a cluster connector to transfer user-defined function calls to a high-performance compute cluster, and for cluster session management.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="6d77c-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="6d77c-109">In this section</span></span>

[<span data-ttu-id="6d77c-110">CallUDF</span><span class="sxs-lookup"><span data-stu-id="6d77c-110">CallUDF</span></span>](calludf.md)
  
[<span data-ttu-id="6d77c-111">CancelOutstandingRequests</span><span class="sxs-lookup"><span data-stu-id="6d77c-111">CancelOutstandingRequests</span></span>](canceloutstandingrequests.md)
  
[<span data-ttu-id="6d77c-112">CloseSession</span><span class="sxs-lookup"><span data-stu-id="6d77c-112">CloseSession</span></span>](closesession.md)
  
[<span data-ttu-id="6d77c-113">OpenSession</span><span class="sxs-lookup"><span data-stu-id="6d77c-113">OpenSession</span></span>](opensession.md)
  
[<span data-ttu-id="6d77c-114">PingSession</span><span class="sxs-lookup"><span data-stu-id="6d77c-114">PingSession</span></span>](pingsession.md)
  
[<span data-ttu-id="6d77c-115">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="6d77c-115">ShowOptions</span></span>](showoptions.md)
  
## <a name="see-also"></a><span data-ttu-id="6d77c-116">Ver también</span><span class="sxs-lookup"><span data-stu-id="6d77c-116">See also</span></span>



[<span data-ttu-id="6d77c-117">Desarrollo de conectores de cl�ster de Excel de 2013</span><span class="sxs-lookup"><span data-stu-id="6d77c-117">Developing Excel Cluster Connectors</span></span>](developing-excel-cluster-connectors.md)
  
[<span data-ttu-id="6d77c-118">Funciones seguras de clúster</span><span class="sxs-lookup"><span data-stu-id="6d77c-118">Cluster Safe Functions</span></span>](cluster-safe-functions.md)

