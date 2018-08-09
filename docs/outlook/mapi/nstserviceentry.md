---
title: NSTServiceEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ada6363-2406-4c0a-8326-a299a8bbefe1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b5902c25197c2ae5790e654a8f29227e107b4a72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818420"
---
# <a name="nstserviceentry"></a><span data-ttu-id="ffb50-103">NSTServiceEntry</span><span class="sxs-lookup"><span data-stu-id="ffb50-103">NSTServiceEntry</span></span>

  
  
<span data-ttu-id="ffb50-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ffb50-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ffb50-105">Función de punto de entrada de servicio de mensajes para una MAPI proveedor para ajustar un almacén local basada en PST como un almacén de NST de almacén.</span><span class="sxs-lookup"><span data-stu-id="ffb50-105">Message service entry point function for a MAPI store provider to wrap a PST-based local store as an NST store.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="ffb50-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="ffb50-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ffb50-107">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="ffb50-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="ffb50-108">Proveedor MAPI</span><span class="sxs-lookup"><span data-stu-id="ffb50-108">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="ffb50-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="ffb50-109">Called by:</span></span>  <br/> |<span data-ttu-id="ffb50-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="ffb50-110">MAPI</span></span>  <br/> |
   
```cpp
HRESULT NSTServiceEntry( 
    HINSTANCE hInstance,   
    LPMALLOC lpMalloc, 
    LPMAPISUP lpMAPISup, 
    ULONG ulUIParam, 
    ULONG ulFlags, 
    ULONG ulContext, 
    ULONG cValues, 
    LPSPropValue lpProps, 
    LPPROVIDERADMIN lpProviderAdmin, 
    LPMAPIERROR FAR * lppMapiError 
);
```

## <a name="parameters"></a><span data-ttu-id="ffb50-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ffb50-111">Parameters</span></span>

 <span data-ttu-id="ffb50-112">**NSTServiceEntry** utiliza el prototipo de función **[MSGSERVICEENTRY](msgserviceentry.md)** .</span><span class="sxs-lookup"><span data-stu-id="ffb50-112">**NSTServiceEntry** uses the **[MSGSERVICEENTRY](msgserviceentry.md)** function prototype.</span></span> <span data-ttu-id="ffb50-113">Para obtener información sobre sus parámetros, consulte **[MSGSERVICEENTRY](msgserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="ffb50-113">For information on its parameters, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="return-values"></a><span data-ttu-id="ffb50-114">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="ffb50-114">Return values</span></span>

<span data-ttu-id="ffb50-115">Para obtener información acerca de los valores devueltos, vea **[MSGSERVICEENTRY](msgserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="ffb50-115">For information on return values, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ffb50-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ffb50-116">Remarks</span></span>

<span data-ttu-id="ffb50-117">Cuando se usa **[GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx)** para buscar la dirección de esta función en msmapi32.dll, especifique "NSTServiceEntry" como el nombre del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="ffb50-117">When using **[GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx)** to look for the address of this function in msmapi32.dll, specify "NSTServiceEntry" as the procedure name.</span></span> 
  
<span data-ttu-id="ffb50-118">Para usar la API de replicación, un proveedor de almacén MAPI en primer lugar debe abrir y se ajusta a un almacén local basada en PST mediante una llamada a **[NSTServiceEntry](nstserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="ffb50-118">To use the Replication API, a MAPI store provider must first open and wrap a PST-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="ffb50-119">El proveedor, a continuación, puede usar las interfaces principales de la API, **[IOSTX](iostxiunknown.md)** y **[IPSTX](ipstxiunknown.md)**, para llevar a cabo la replicación.</span><span class="sxs-lookup"><span data-stu-id="ffb50-119">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> 
  
<span data-ttu-id="ffb50-120">Los siguientes comentarios son aplicables a un almacén de NST:</span><span class="sxs-lookup"><span data-stu-id="ffb50-120">The following remarks apply to an NST store:</span></span>
  
- <span data-ttu-id="ffb50-121">No almacene ninguna información en la sección perfil global al implementar un proveedor MAPI que usa **NSTServiceEntry**.</span><span class="sxs-lookup"><span data-stu-id="ffb50-121">Do not store any information in the global profile section when implementing a MAPI provider that uses **NSTServiceEntry**.</span></span> <span data-ttu-id="ffb50-122">La sección de perfil global es compartida por muchos de los proveedores y se pueden sobrescribir los datos almacenados en este perfil.</span><span class="sxs-lookup"><span data-stu-id="ffb50-122">The global profile section is shared by many providers and data stored in this profile can be overwritten.</span></span> 
    
- <span data-ttu-id="ffb50-123">Sólo los elementos con marcas de hora de modificación existente obtienen sus marcas que se actualizan cuando se guardan.</span><span class="sxs-lookup"><span data-stu-id="ffb50-123">Only items with existing modification time stamps get their stamps updated when they are saved.</span></span> 
    
- <span data-ttu-id="ffb50-124">Comprobación de conflictos no se producen automáticamente cuando se guardan los elementos.</span><span class="sxs-lookup"><span data-stu-id="ffb50-124">Conflict-checking does not occur automatically when items are saved.</span></span>
    
-  <span data-ttu-id="ffb50-125">Detección de duplicados no se produce cuando se guardan los elementos.</span><span class="sxs-lookup"><span data-stu-id="ffb50-125">Duplicate detection does not occur when items are saved.</span></span> 
    
-  <span data-ttu-id="ffb50-126">Se agrega el archivo que representa la versión almacenada en caché del servidor. NST.</span><span class="sxs-lookup"><span data-stu-id="ffb50-126">The file representing the cached version of the server is appended with .NST.</span></span> 
    
- <span data-ttu-id="ffb50-127">Para obtener un puntero a la sección de perfil global, un servicio de mensajes llama a **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** en el objeto de soporte técnico mediante **pbNSTGlobalProfileSectionGuid** tal como se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="ffb50-127">To obtain a pointer to the global profile section, a message service calls **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** in the support object using **pbNSTGlobalProfileSectionGuid** as defined below:</span></span> 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- <span data-ttu-id="ffb50-128">En este caso, el objeto de soporte técnico del servicio de mensajes debe asegurarse de que **IMAPISupport::OpenProfileSection** devuelve la sección de perfil que se identifica con la propiedad **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** en la sección de perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ffb50-128">In this case, the support object of the message service should ensure that **IMAPISupport::OpenProfileSection** returns the profile section that is identified by the **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** property in the default profile section.</span></span> <span data-ttu-id="ffb50-129">Para obtener esta sección de perfil, el objeto de soporte técnico puede abrir la sección de perfil predeterminado, recuperar **PR_SERVICE_UID**y pasa el resultado a **IMAPISupport::OpenProfileSection** para recuperar la sección de perfil global correcto.</span><span class="sxs-lookup"><span data-stu-id="ffb50-129">To get this profile section, the support object can open the default profile section, retrieve **PR_SERVICE_UID**, and pass the result to **IMAPISupport::OpenProfileSection** to retrieve the correct global profile section.</span></span> <span data-ttu-id="ffb50-130">El objeto de soporte a su vez devuelve un puntero a esta sección de perfil global para el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ffb50-130">The support object in turn returns a pointer to this global profile section to the message service.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ffb50-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="ffb50-131">See also</span></span>



[<span data-ttu-id="ffb50-132">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="ffb50-132">About the Replication API</span></span>](about-the-replication-api.md)

