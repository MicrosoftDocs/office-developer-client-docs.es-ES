---
title: Desarrollo de conectores de clúster de Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e1c70713586a7a143f119a2c3e9d34b982dcedba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412600"
---
# <a name="developing-excel-cluster-connectors"></a><span data-ttu-id="ac771-103">Desarrollo de conectores de clúster de Excel</span><span class="sxs-lookup"><span data-stu-id="ac771-103">Developing Excel Cluster Connectors</span></span>

<span data-ttu-id="ac771-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ac771-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ac771-105">Los conectores de clúster de Excel proporcionan un medio para descargar automáticamente las llamadas de funciones definidas por el usuario seguras para clústeres en un XLL a un servidor agrupado.</span><span class="sxs-lookup"><span data-stu-id="ac771-105">Excel cluster connectors provide a means for automatically offloading cluster-safe user-defined function calls in an XLL to a clustered server.</span></span> <span data-ttu-id="ac771-106">Para obtener una descripción de las funciones definidas por el usuario seguras para clústeres, consulte [cluster Safe Functions](cluster-safe-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ac771-106">For a description of cluster-safe user-defined functions, see [Cluster Safe Functions](cluster-safe-functions.md).</span></span> <span data-ttu-id="ac771-107">Esta descarga puede mejorar el rendimiento al permitir que se usen más recursos informáticos.</span><span class="sxs-lookup"><span data-stu-id="ac771-107">This offloading can improve performance by enabling more computing resources to be used.</span></span> <span data-ttu-id="ac771-108">Un conector de clúster suele ser desarrollado por un proveedor de clústeres de cómputo de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="ac771-108">A cluster connector is typically developed by a high performance compute cluster vendor.</span></span>
  
## <a name="cluster-connectors"></a><span data-ttu-id="ac771-109">Conectores de clúster</span><span class="sxs-lookup"><span data-stu-id="ac771-109">Cluster Connectors</span></span>

<span data-ttu-id="ac771-110">Un conector de clúster es una DLL que proporciona puntos de entrada definidos que Excel usa para coordinar llamadas de función definidas por el usuario seguras para clústeres.</span><span class="sxs-lookup"><span data-stu-id="ac771-110">A cluster connector is a DLL that provides defined entry points that Excel uses to coordinate cluster-safe user-defined function calls.</span></span> <span data-ttu-id="ac771-111">Actúa como una interfaz entre Excel y el clúster de cómputo de alto rendimiento, para la administración de sesiones, para realizar llamadas de función (pasando el nombre completo de la función y los argumentos reales de la llamada) y devolver los resultados de la llamada a Excel a través de un mecanismo de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="ac771-111">It serves as an interface between Excel and the high-performance compute cluster, for session management, for making function calls (by passing the fully-qualified function name and the call's actual arguments), and for returning call results to Excel through a callback mechanism.</span></span>
  
<span data-ttu-id="ac771-112">Para crear un conector de clúster, cree un archivo DLL que exponga los puntos de entrada enumerados en [funciones de conector de clúster de Excel](excel-cluster-connector-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ac771-112">To create a cluster connector, create a DLL that exposes the entry points listed in [Excel Cluster Connector Functions](excel-cluster-connector-functions.md).</span></span>
  
## <a name="installing-a-cluster-connector"></a><span data-ttu-id="ac771-113">Instalación de un conector de clúster</span><span class="sxs-lookup"><span data-stu-id="ac771-113">Installing a Cluster Connector</span></span>

<span data-ttu-id="ac771-114">Para que un conector de clúster esté disponible en Excel, el código del programa de instalación del conector debe instalar la DLL del conector en el equipo en el que está instalado Excel.</span><span class="sxs-lookup"><span data-stu-id="ac771-114">To make a cluster connector available in Excel, the setup code of the connector must install the DLL of the connector on the computer where Excel is installed.</span></span> <span data-ttu-id="ac771-115">Además, el código del programa de instalación del conector debe agregar una entrada para el conector en la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="ac771-115">In addition, the setup code of the connector must add an entry for the connector under the following registry key:</span></span>
  
<span data-ttu-id="ac771-116">Conectores de clúster de HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel \\</span><span class="sxs-lookup"><span data-stu-id="ac771-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\\</span></span>
  
<span data-ttu-id="ac771-117">Agregue un nodo a esta clave para el conector de clúster que especifica las siguientes cadenas:</span><span class="sxs-lookup"><span data-stu-id="ac771-117">Add a node to this key for the cluster connector that specifies the following strings:</span></span>
  
-  <span data-ttu-id="ac771-118">`Name`: el nombre que aparecerá en la lista de conectores de clúster en Excel.</span><span class="sxs-lookup"><span data-stu-id="ac771-118">`Name`—the name that will appear in the list of cluster connectors in Excel.</span></span>
    
-  <span data-ttu-id="ac771-119">`Filename`: la ruta de acceso completa del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="ac771-119">`Filename`—the full path for the DLL.</span></span>
    

