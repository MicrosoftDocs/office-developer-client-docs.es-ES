---
title: Registrar servicios y proveedores de servicios en MapiSvc. inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Última modificación: 18 de julio de 2013'
ms.openlocfilehash: adc6318ab36818b4c423bb6b1dc1b083b3fb54eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328374"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a><span data-ttu-id="e442f-103">Registrar servicios y proveedores de servicios en MapiSvc. inf</span><span class="sxs-lookup"><span data-stu-id="e442f-103">Registering Services and Service Providers in MapiSvc.inf</span></span>

 
  
<span data-ttu-id="e442f-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e442f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e442f-105">Para instalar un nuevo proveedor en un sistema, es necesario actualizar el archivo MapiSvc. inf para que apunte al nuevo proveedor.</span><span class="sxs-lookup"><span data-stu-id="e442f-105">Installing a new provider on a system requires updating the MapiSvc.inf file to point to the new provider.</span></span> <span data-ttu-id="e442f-106">Las propiedades estándar establecidas durante la configuración, entre las que se incluyen las siguientes, informan a MAPI dónde encontrar la biblioteca de vínculos dinámicos del proveedor (. dll):</span><span class="sxs-lookup"><span data-stu-id="e442f-106">Standard properties set during configuration, which include the following, inform MAPI where to find the provider's dynamic-link library (.dll):</span></span>
  
- <span data-ttu-id="e442f-107">La **PR_SERVICE_DLL_NAME** se especifica en la sección **[Message Service]** .</span><span class="sxs-lookup"><span data-stu-id="e442f-107">The **PR_SERVICE_DLL_NAME** is specified in the **[Message Service]** section.</span></span> 
    
- <span data-ttu-id="e442f-108">La **PR_PROVIDER_DLL_NAME** se especifica en la sección **[proveedor de servicios]** .</span><span class="sxs-lookup"><span data-stu-id="e442f-108">The **PR_PROVIDER_DLL_NAME** is specified in the **[Service Provider]** section.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="e442f-109">La expectativa es que establezca el nombre del archivo. dll de su proveedor (sin el sufijo "32").</span><span class="sxs-lookup"><span data-stu-id="e442f-109">The expectation is that you set the name of your provider's .dll (without the suffix "32").</span></span> <span data-ttu-id="e442f-110">MAPI, a continuación, carga el proveedor buscándolo en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="e442f-110">MAPI then loads your provider by looking for it on the path.</span></span> 
  
## <a name="putting-a-path-in-mapisvcinf"></a><span data-ttu-id="e442f-111">Poner una ruta de acceso en MapiSvc. inf</span><span class="sxs-lookup"><span data-stu-id="e442f-111">Putting a Path in MapiSvc.inf</span></span>

<span data-ttu-id="e442f-112">La mayoría de las aplicaciones se instalan en archivos de programa, lo que requiere una actualización a la variable PATH para permitir que los proveedores MAPI funcionen.</span><span class="sxs-lookup"><span data-stu-id="e442f-112">Most applications install under Program Files, requiring an update to the path variable to allow MAPI providers to work.</span></span> <span data-ttu-id="e442f-113">Con algunas restricciones, Microsoft Outlook 2010 y Outlook 2013 pueden admitir rutas completas a los proveedores MAPI.</span><span class="sxs-lookup"><span data-stu-id="e442f-113">With a few restrictions Microsoft Outlook 2010 and Outlook 2013 can accommodate full paths to MAPI providers.</span></span>
  
<span data-ttu-id="e442f-114">Al registrar el proveedor en MapiSvc. inf, puede incluir la ruta de acceso completa en el proveedor en las propiedades MAPI **PR_SERVICE_DLL_NAME** y **PR_PROVIDER_DLL_NAME**.</span><span class="sxs-lookup"><span data-stu-id="e442f-114">When registering your provider in MapiSvc.inf, you could put the full path to the provider in the MAPI properties **PR_SERVICE_DLL_NAME** and **PR_PROVIDER_DLL_NAME**.</span></span>
  
<span data-ttu-id="e442f-115">En cualquiera de las dos propiedades, la ruta de acceso completa debe estar sin el sufijo "32", ya que MAPI continuará anexando esa al nombre de archivo antes de buscar el archivo.</span><span class="sxs-lookup"><span data-stu-id="e442f-115">In either property, the full path must be without the suffix "32", because MAPI continues to append that to the filename before looking for your file.</span></span> <span data-ttu-id="e442f-116">Esto significa que si registra la ruta "c:\mypath\myprovider.dll", MAPI intentará cargar "c:\mypath\myprovider32.dll".</span><span class="sxs-lookup"><span data-stu-id="e442f-116">This means that if you register the path "c:\mypath\myprovider.dll", MAPI will attempt to load "c:\mypath\myprovider32.dll".</span></span>
  
<span data-ttu-id="e442f-117">Como MAPI de Outlook no se diseñó originalmente para dar cabida a rutas de todas las rutas, realiza esta inserción del sufijo "32" buscando el primer punto de la cadena, lo que significa que las rutas que contienen otros períodos no pueden funcionar, por lo que no puede usar rutas como "c:\my.path\myprovider.dll" o "c:\mypath\my.Provider.dll".</span><span class="sxs-lookup"><span data-stu-id="e442f-117">Because Outlook's MAPI was not originally designed to accommodate full paths, it accomplishes this insertion of the "32" suffix by looking for the first period in the string, which means that paths that contain other periods cannot work, so you cannot use paths such as "c:\my.path\myprovider.dll" or "c:\mypath\my.provider.dll".</span></span>
  
<span data-ttu-id="e442f-118">A veces, en un proveedor de almacenamiento generará identificadores de entrada mediante la función **WrapStoreEntryID** , que toma como parámetro el nombre de su proveedor.</span><span class="sxs-lookup"><span data-stu-id="e442f-118">Sometimes in a store provider you will generate entry identifiers using the **WrapStoreEntryID** function, which takes as a parameter the name of your provider.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="e442f-119">Si está usando rutas completas en MapiSvc. inf, debe usar la misma ruta de acceso en cualquier llamada a **WrapStoreEntryID**.</span><span class="sxs-lookup"><span data-stu-id="e442f-119">If you are using full paths in MapiSvc.inf, you must use the same path in any calls to **WrapStoreEntryID**.</span></span> 
  
<span data-ttu-id="e442f-120">Además, la ruta de acceso que use se puede convertir a y desde Unicode mediante la página de códigos proporcionada por la función [GetACP](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) .</span><span class="sxs-lookup"><span data-stu-id="e442f-120">Additionally, the path you use may be converted to and from Unicode using the code page provided by the [GetACP](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) function.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="e442f-121">Experimentará un error si elige una ruta de acceso que contiene caracteres que no pueden sobrevivir a este tipo de ida y vuelta a través de las funciones [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) y [WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) .</span><span class="sxs-lookup"><span data-stu-id="e442f-121">You will experience failure if you choose a path that contains characters that cannot survive such a roundtrip through the [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) and [WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) functions.</span></span> 
  
<span data-ttu-id="e442f-122">Para una demostración de esta funcionalidad, se ha revisado el [ejemplo de PST ajustado](https://github.com/stephenegriffin/Outlook2010CodeSamples) en github: la funcionalidad correspondiente está en **MergeWithMapiSvc** y **GenerateProviderPath**.</span><span class="sxs-lookup"><span data-stu-id="e442f-122">For a demonstration of this functionality, the [Wrapped PST sample](https://github.com/stephenegriffin/Outlook2010CodeSamples) on GitHub has been revised - the pertinent functionality is in **MergeWithMapiSvc** and **GenerateProviderPath**.</span></span>
  

