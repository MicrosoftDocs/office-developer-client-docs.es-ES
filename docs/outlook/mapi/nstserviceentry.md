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
ms.openlocfilehash: 96c04a242c477204ea1447fb78c31d189eeac59a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280057"
---
# <a name="nstserviceentry"></a><span data-ttu-id="219e5-103">NSTServiceEntry</span><span class="sxs-lookup"><span data-stu-id="219e5-103">NSTServiceEntry</span></span>

  
  
<span data-ttu-id="219e5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="219e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="219e5-105">Función de punto de entrada del servicio de mensajes para que un proveedor de almacén MAPI ajuste un almacén local basado en PST como un almacén NST.</span><span class="sxs-lookup"><span data-stu-id="219e5-105">Message service entry point function for a MAPI store provider to wrap a PST-based local store as an NST store.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="219e5-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="219e5-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="219e5-107">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="219e5-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="219e5-108">Proveedor MAPI</span><span class="sxs-lookup"><span data-stu-id="219e5-108">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="219e5-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="219e5-109">Called by:</span></span>  <br/> |<span data-ttu-id="219e5-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="219e5-110">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="219e5-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="219e5-111">Parameters</span></span>

 <span data-ttu-id="219e5-112">**NSTServiceEntry usa** el prototipo **[de función MSGSERVICEENTRY.](msgserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="219e5-112">**NSTServiceEntry** uses the **[MSGSERVICEENTRY](msgserviceentry.md)** function prototype.</span></span> <span data-ttu-id="219e5-113">Para obtener información sobre sus parámetros, vea **[MSGSERVICEENTRY](msgserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="219e5-113">For information on its parameters, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="return-values"></a><span data-ttu-id="219e5-114">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="219e5-114">Return values</span></span>

<span data-ttu-id="219e5-115">Para obtener información sobre los valores devueltos, vea **[MSGSERVICEENTRY](msgserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="219e5-115">For information on return values, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="219e5-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="219e5-116">Remarks</span></span>

<span data-ttu-id="219e5-117">Al usar **[GetProcAddress para](https://msdn.microsoft.com/library/ms683212.aspx)** buscar la dirección de esta función en msmapi32.dll, especifique "NSTServiceEntry" como nombre del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="219e5-117">When using **[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** to look for the address of this function in msmapi32.dll, specify "NSTServiceEntry" as the procedure name.</span></span> 
  
<span data-ttu-id="219e5-118">Para usar la API de replicación, un proveedor de almacén MAPI primero debe abrir y encapsular un almacén local basado en PST llamando a **[NSTServiceEntry](nstserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="219e5-118">To use the Replication API, a MAPI store provider must first open and wrap a PST-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="219e5-119">A continuación, el proveedor puede usar las interfaces principales de la API, **[IOSTX](iostxiunknown.md)** e **[IPSTX,](ipstxiunknown.md)** para llevar a cabo la replicación.</span><span class="sxs-lookup"><span data-stu-id="219e5-119">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> 
  
<span data-ttu-id="219e5-120">Las siguientes observaciones se aplican a un almacén NST:</span><span class="sxs-lookup"><span data-stu-id="219e5-120">The following remarks apply to an NST store:</span></span>
  
- <span data-ttu-id="219e5-121">No almacene información en la sección de perfil global al implementar un proveedor MAPI que use **NSTServiceEntry**.</span><span class="sxs-lookup"><span data-stu-id="219e5-121">Do not store any information in the global profile section when implementing a MAPI provider that uses **NSTServiceEntry**.</span></span> <span data-ttu-id="219e5-122">Muchos proveedores comparten la sección de perfil global y los datos almacenados en este perfil se pueden sobrescribir.</span><span class="sxs-lookup"><span data-stu-id="219e5-122">The global profile section is shared by many providers and data stored in this profile can be overwritten.</span></span> 
    
- <span data-ttu-id="219e5-123">Solo los elementos con marcas de tiempo de modificación existentes obtienen sus marcas actualizadas cuando se guardan.</span><span class="sxs-lookup"><span data-stu-id="219e5-123">Only items with existing modification time stamps get their stamps updated when they are saved.</span></span> 
    
- <span data-ttu-id="219e5-124">La comprobación de conflictos no se produce automáticamente cuando se guardan los elementos.</span><span class="sxs-lookup"><span data-stu-id="219e5-124">Conflict-checking does not occur automatically when items are saved.</span></span>
    
-  <span data-ttu-id="219e5-125">La detección de duplicados no se produce cuando se guardan los elementos.</span><span class="sxs-lookup"><span data-stu-id="219e5-125">Duplicate detection does not occur when items are saved.</span></span> 
    
-  <span data-ttu-id="219e5-126">El archivo que representa la versión almacenada en caché del servidor se anexa con . NST.</span><span class="sxs-lookup"><span data-stu-id="219e5-126">The file representing the cached version of the server is appended with .NST.</span></span> 
    
- <span data-ttu-id="219e5-127">Para obtener un puntero a la sección de perfil global, un servicio de mensajes llama a **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** en el objeto de compatibilidad mediante **pbNSTGlobalProfileSectionGuid** como se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="219e5-127">To obtain a pointer to the global profile section, a message service calls **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** in the support object using **pbNSTGlobalProfileSectionGuid** as defined below:</span></span> 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- <span data-ttu-id="219e5-128">En este caso, el objeto de compatibilidad del servicio de mensajes debe asegurarse de que **IMAPISupport::OpenProfileSection** devuelve la sección de perfil identificada por la propiedad **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** en la sección de perfil predeterminada.</span><span class="sxs-lookup"><span data-stu-id="219e5-128">In this case, the support object of the message service should ensure that **IMAPISupport::OpenProfileSection** returns the profile section that is identified by the **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** property in the default profile section.</span></span> <span data-ttu-id="219e5-129">Para obtener esta sección de perfil, el objeto de soporte puede abrir la sección de perfil predeterminada, recuperar PR_SERVICE_UID y pasar el resultado **a** **IMAPISupport::OpenProfileSection** para recuperar la sección de perfil global correcta.</span><span class="sxs-lookup"><span data-stu-id="219e5-129">To get this profile section, the support object can open the default profile section, retrieve **PR_SERVICE_UID**, and pass the result to **IMAPISupport::OpenProfileSection** to retrieve the correct global profile section.</span></span> <span data-ttu-id="219e5-130">A su vez, el objeto de soporte devuelve un puntero a esta sección de perfil global al servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="219e5-130">The support object in turn returns a pointer to this global profile section to the message service.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="219e5-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="219e5-131">See also</span></span>



[<span data-ttu-id="219e5-132">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="219e5-132">About the Replication API</span></span>](about-the-replication-api.md)

