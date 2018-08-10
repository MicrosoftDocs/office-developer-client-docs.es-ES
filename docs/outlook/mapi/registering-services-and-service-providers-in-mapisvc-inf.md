---
title: Registrar servicios y proveedores de servicios en MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Última modificación: 18 de julio de 2013'
ms.openlocfilehash: 2eb7f1b496e0732b157ea4f9105a0e067329c52f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820490"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a><span data-ttu-id="83719-103">Registrar servicios y proveedores de servicios en MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="83719-103">Registering Services and Service Providers in MapiSvc.inf</span></span>

 
  
<span data-ttu-id="83719-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="83719-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="83719-105">Instalación de un nuevo proveedor en un sistema requiere la actualización del archivo MapiSvc.inf para que apunte al nuevo proveedor.</span><span class="sxs-lookup"><span data-stu-id="83719-105">Installing a new provider on a system requires updating the MapiSvc.inf file to point to the new provider.</span></span> <span data-ttu-id="83719-106">Las propiedades estándar establecer durante la configuración, que se incluyen los siguientes, informar a MAPI dónde encontrar la biblioteca de vínculos dinámicos (.dll) de un proveedor:</span><span class="sxs-lookup"><span data-stu-id="83719-106">Standard properties set during configuration, which include the following, inform MAPI where to find the provider's dynamic-link library (.dll):</span></span>
  
- <span data-ttu-id="83719-107">El **PR_SERVICE_DLL_NAME** se especifica en la sección **[Servicio de mensajes]** .</span><span class="sxs-lookup"><span data-stu-id="83719-107">The **PR_SERVICE_DLL_NAME** is specified in the **[Message Service]** section.</span></span> 
    
- <span data-ttu-id="83719-108">El **PR_PROVIDER_DLL_NAME** se especifica en la sección **[Servicio proveedor]** .</span><span class="sxs-lookup"><span data-stu-id="83719-108">The **PR_PROVIDER_DLL_NAME** is specified in the **[Service Provider]** section.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="83719-109">La expectativa es establecer el nombre de .dll su proveedor (sin el sufijo "32").</span><span class="sxs-lookup"><span data-stu-id="83719-109">The expectation is that you set the name of your provider's .dll (without the suffix "32").</span></span> <span data-ttu-id="83719-110">MAPI, a continuación, carga el proveedor busca en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="83719-110">MAPI then loads your provider by looking for it on the path.</span></span> 
  
## <a name="putting-a-path-in-mapisvcinf"></a><span data-ttu-id="83719-111">Colocando una ruta de acceso en MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="83719-111">Putting a Path in MapiSvc.inf</span></span>

<span data-ttu-id="83719-112">Instalarán la mayoría de las aplicaciones en archivos de programa, que requieren una actualización a la variable de ruta de acceso para permitir que los proveedores de MAPI para que funcione.</span><span class="sxs-lookup"><span data-stu-id="83719-112">Most applications install under Program Files, requiring an update to the path variable to allow MAPI providers to work.</span></span> <span data-ttu-id="83719-113">Con unas cuantas restricciones Microsoft Outlook 2010 y Outlook 2013 pueden dar cabida a rutas de acceso completas a proveedores de MAPI.</span><span class="sxs-lookup"><span data-stu-id="83719-113">With a few restrictions Microsoft Outlook 2010 and Outlook 2013 can accommodate full paths to MAPI providers.</span></span>
  
<span data-ttu-id="83719-114">Al registrar el proveedor en MapiSvc.inf, podría colocar la ruta de acceso completa para el proveedor en las propiedades MAPI **PR_SERVICE_DLL_NAME** y **PR_PROVIDER_DLL_NAME**.</span><span class="sxs-lookup"><span data-stu-id="83719-114">When registering your provider in MapiSvc.inf, you could put the full path to the provider in the MAPI properties **PR_SERVICE_DLL_NAME** and **PR_PROVIDER_DLL_NAME**.</span></span>
  
<span data-ttu-id="83719-115">En cualquiera de estas propiedades, debe ser la ruta de acceso completa sin el sufijo "32", debido a que continúa MAPI anexar al nombre del archivo antes de buscar el archivo.</span><span class="sxs-lookup"><span data-stu-id="83719-115">In either property, the full path must be without the suffix "32", because MAPI continues to append that to the filename before looking for your file.</span></span> <span data-ttu-id="83719-116">Esto significa que si se registra la ruta de acceso "c:\mypath\myprovider.dll", MAPI intentará cargar "c:\mypath\myprovider32.dll".</span><span class="sxs-lookup"><span data-stu-id="83719-116">This means that if you register the path "c:\mypath\myprovider.dll", MAPI will attempt to load "c:\mypath\myprovider32.dll".</span></span>
  
<span data-ttu-id="83719-117">Debido a que Outlook MAPI no se diseñó originalmente para dar cabida a rutas de acceso completas, lleva a cabo esta inserción del sufijo "32" buscando el primer período en la cadena, lo que significa que no funcionan las rutas de acceso que contienen otros períodos, por lo que no puede usar como rutas de acceso "c:\my.path\myprovider.dll" o "c:\mypath\my.provider.dll".</span><span class="sxs-lookup"><span data-stu-id="83719-117">Because Outlook's MAPI was not originally designed to accommodate full paths, it accomplishes this insertion of the "32" suffix by looking for the first period in the string, which means that paths that contain other periods cannot work, so you cannot use paths such as "c:\my.path\myprovider.dll" or "c:\mypath\my.provider.dll".</span></span>
  
<span data-ttu-id="83719-118">A veces en un proveedor de almacén generará mediante la función **WrapStoreEntryID** , que toma como parámetro el nombre del proveedor de los identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="83719-118">Sometimes in a store provider you will generate entry identifiers using the **WrapStoreEntryID** function, which takes as a parameter the name of your provider.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="83719-119">Si está utilizando rutas de acceso completas en MapiSvc.inf, debe usar la misma ruta de acceso en todas las llamadas a **WrapStoreEntryID**.</span><span class="sxs-lookup"><span data-stu-id="83719-119">If you are using full paths in MapiSvc.inf, you must use the same path in any calls to **WrapStoreEntryID**.</span></span> 
  
<span data-ttu-id="83719-120">Además, la ruta de acceso que se utiliza es posible que se va a convertir a y desde Unicode mediante la página de código proporcionada por la función [GetACP](http://msdn.microsoft.com/en-us/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) .</span><span class="sxs-lookup"><span data-stu-id="83719-120">Additionally, the path you use may be converted to and from Unicode using the code page provided by the [GetACP](http://msdn.microsoft.com/en-us/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) function.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="83719-121">Si elige una ruta de acceso que contiene caracteres que no se pueden sobrevivir fácilmente a través de las funciones de [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) y [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) experimentará errores.</span><span class="sxs-lookup"><span data-stu-id="83719-121">You will experience failure if you choose a path that contains characters that cannot survive such a roundtrip through the [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) and [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) functions.</span></span> 
  
<span data-ttu-id="83719-122">Para una demostración de esta funcionalidad, se ha revisado el [ejemplo PST ajustado](http://ol2010mapisamples.codeplex.com/) en CodePlex - la funcionalidad pertinente se encuentra en **MergeWithMapiSvc** y **GenerateProviderPath**.</span><span class="sxs-lookup"><span data-stu-id="83719-122">For a demonstration of this functionality, the [Wrapped PST sample](http://ol2010mapisamples.codeplex.com/) on CodePlex has been revised - the pertinent functionality is in **MergeWithMapiSvc** and **GenerateProviderPath**.</span></span>
  

