---
title: Desarrollo de conectores de clúster de Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8c9a166ac06685c0a450e1e0bd60b2fbef67d336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815517"
---
# <a name="developing-excel-cluster-connectors"></a><span data-ttu-id="d6e5e-103">Desarrollo de conectores de clúster de Excel</span><span class="sxs-lookup"><span data-stu-id="d6e5e-103">Developing Excel Cluster Connectors</span></span>

<span data-ttu-id="d6e5e-104">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d6e5e-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d6e5e-105">Conectores de clúster de Excel proporcionan un medio para descarga automáticamente las llamadas de función definida por el usuario con seguridad de clúster en un XLL a un servidor de clúster.</span><span class="sxs-lookup"><span data-stu-id="d6e5e-105">Excel cluster connectors provide a means for automatically offloading cluster-safe user-defined function calls in an XLL to a clustered server.</span></span> <span data-ttu-id="d6e5e-106">Para obtener una descripción de las funciones definidas por el usuario de seguras de clúster, vea [Funciones seguras de clúster](cluster-safe-functions.md).</span><span class="sxs-lookup"><span data-stu-id="d6e5e-106">For a description of cluster-safe user-defined functions, see [Cluster Safe Functions](cluster-safe-functions.md).</span></span> <span data-ttu-id="d6e5e-107">Esta descarga puede mejorar el rendimiento mediante la habilitación de más recursos informáticos que se usará.</span><span class="sxs-lookup"><span data-stu-id="d6e5e-107">This offloading can improve performance by enabling more computing resources to be used.</span></span> <span data-ttu-id="d6e5e-108">Un conector de clúster normalmente está desarrollado por un proveedor de clúster de cálculo de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="d6e5e-108">A cluster connector is typically developed by a high performance compute cluster vendor.</span></span>
  
## <a name="cluster-connectors"></a><span data-ttu-id="d6e5e-109">Conectores de clúster</span><span class="sxs-lookup"><span data-stu-id="d6e5e-109">Cluster Connectors</span></span>

<span data-ttu-id="d6e5e-110">Un conector de clúster es un archivo DLL que proporciona puntos de entrada definido que Excel utiliza para coordinar las llamadas de función definida por el usuario con seguridad de clúster.</span><span class="sxs-lookup"><span data-stu-id="d6e5e-110">A cluster connector is a DLL that provides defined entry points that Excel uses to coordinate cluster-safe user-defined function calls.</span></span> <span data-ttu-id="d6e5e-111">Sirve como una interfaz entre Excel y el clúster de cálculo de alto rendimiento, para la sesión de administración, para hacer que la función se llama (pasando el nombre de función completo y argumentos reales de la llamada) y para devolver los resultados de la llamada a Excel a través de una mecanismo de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="d6e5e-111">It serves as an interface between Excel and the high-performance compute cluster, for session management, for making function calls (by passing the fully-qualified function name and the call's actual arguments), and for returning call results to Excel through a callback mechanism.</span></span>
  
<span data-ttu-id="d6e5e-112">Para crear un conector de clúster, cree un archivo DLL que expone los puntos de entrada que aparecen en las [Funciones de conector de clúster de Excel](excel-cluster-connector-functions.md).</span><span class="sxs-lookup"><span data-stu-id="d6e5e-112">To create a cluster connector, create a DLL that exposes the entry points listed in [Excel Cluster Connector Functions](excel-cluster-connector-functions.md).</span></span>
  
## <a name="installing-a-cluster-connector"></a><span data-ttu-id="d6e5e-113">Instalar un conector de clúster</span><span class="sxs-lookup"><span data-stu-id="d6e5e-113">Installing a Cluster Connector</span></span>

<span data-ttu-id="d6e5e-114">Para hacer que un conector de clúster disponibles en Excel, el código del programa de instalación del conector debe instalar el archivo DLL del conector en el equipo donde está instalado Excel.</span><span class="sxs-lookup"><span data-stu-id="d6e5e-114">To make a cluster connector available in Excel, the setup code of the connector must install the DLL of the connector on the computer where Excel is installed.</span></span> <span data-ttu-id="d6e5e-115">Además, el código del programa de instalación del conector debe agregar una entrada para el conector en la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="d6e5e-115">In addition, the setup code of the connector must add an entry for the connector under the following registry key:</span></span>
  
<span data-ttu-id="d6e5e-116">Connectors\ de clúster HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel</span><span class="sxs-lookup"><span data-stu-id="d6e5e-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\\</span></span>
  
<span data-ttu-id="d6e5e-117">Agregar un nodo a esta clave para el conector de clúster que especifica las siguientes cadenas:</span><span class="sxs-lookup"><span data-stu-id="d6e5e-117">Add a node to this key for the cluster connector that specifies the following strings:</span></span>
  
-  <span data-ttu-id="d6e5e-118">`Name`: el nombre que aparecerá en la lista de conectores de clúster en Excel.</span><span class="sxs-lookup"><span data-stu-id="d6e5e-118">`Name`—the name that will appear in the list of cluster connectors in Excel.</span></span>
    
-  <span data-ttu-id="d6e5e-119">`Filename`: la ruta de acceso completa para el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="d6e5e-119">`Filename`—the full path for the DLL.</span></span>
    

