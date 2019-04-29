---
title: Usar un proveedor de almacén de archivos PST ajustado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Última modificación: 3 de julio de 2012'
ms.openlocfilehash: b7c651044ab7f4cad7032db69e157c9a3589bde9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420825"
---
# <a name="using-a-wrapped-pst-store-provider"></a><span data-ttu-id="0d0ff-103">Usar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="0d0ff-103">Using a wrapped PST store provider</span></span>

<span data-ttu-id="0d0ff-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d0ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d0ff-105">Para poder usar un proveedor de almacenamiento de archivos de carpetas personales (PST) ajustado, debe inicializar y configurar el proveedor de almacenamiento de PST ajustado.</span><span class="sxs-lookup"><span data-stu-id="0d0ff-105">Before you can use a wrapped Personal Folders file (PST) store provider, you must initialize and configure the wrapped PST store provider.</span></span> <span data-ttu-id="0d0ff-106">Una vez configurado el proveedor de almacén de archivos PST ajustado, debe implementar funciones para que MAPI y la cola MAPI puedan iniciar sesión en el proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0d0ff-106">After the wrapped PST store provider is configured, you must implement functions so that MAPI and the MAPI spooler can log on to the message store provider.</span></span> <span data-ttu-id="0d0ff-107">Para obtener más información acerca de la inicialización y el inicio de sesión en un proveedor de almacén de archivos PST ajustado, vea [inicializar un proveedor de almacén](initializing-a-wrapped-pst-store-provider.md) de archivos PST ajustado e [iniciar sesión en un proveedor de almacén de archivos PST ajustado](logging-on-to-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0d0ff-107">For more information about initializing and logging on to a wrapped PST store provider, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md) and [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="0d0ff-108">La interfaz **[IMAPISupport:: IUnknown](imapisupportiunknown.md)** proporciona implementaciones para tareas que suelen realizar los proveedores de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0d0ff-108">The **[IMAPISupport::IUnknown](imapisupportiunknown.md)** interface provides implementations for tasks that are commonly performed by message store providers.</span></span> <span data-ttu-id="0d0ff-109">Esta interfaz debe estar ajustada para que funcione el proveedor de almacén de archivos PST ajustado de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0d0ff-109">This interface must be wrapped for the Sample Wrapped PST Store Provider to work.</span></span> <span data-ttu-id="0d0ff-110">La función **[IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md)** requiere una implementación especial.</span><span class="sxs-lookup"><span data-stu-id="0d0ff-110">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function requires special implementation.</span></span> <span data-ttu-id="0d0ff-111">Todas las demás funciones pueden pasar sus parámetros al objeto ajustado subyacente.</span><span class="sxs-lookup"><span data-stu-id="0d0ff-111">All other functions can pass their parameters to the underlying wrapped object.</span></span> 
  
<span data-ttu-id="0d0ff-112">En este tema, la función **IMAPISupport:: OpenProfileSection** se muestra mediante un ejemplo de código del proveedor de almacenamiento PST ajustado del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0d0ff-112">In this topic, the **IMAPISupport::OpenProfileSection** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="0d0ff-113">El ejemplo implementa un proveedor de archivos PST ajustado que está pensado para usarse junto con la API de replicación.</span><span class="sxs-lookup"><span data-stu-id="0d0ff-113">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="0d0ff-114">Para obtener más información sobre cómo descargar e instalar el proveedor de almacén de archivos PST ajustado de ejemplo, vea [Installing the Sample wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0d0ff-114">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="0d0ff-115">Para obtener más información acerca de la API de replicación, consulte [About the replicaTION API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="0d0ff-115">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="0d0ff-116">Cuando termine de usar un proveedor de almacén de archivos PST ajustado, debe apagar correctamente el proveedor de almacén de archivos PST ajustado.</span><span class="sxs-lookup"><span data-stu-id="0d0ff-116">When you finish using a wrapped PST store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="0d0ff-117">Para obtener más información, vea [apagar un proveedor de almacenamiento PST ajustado](shutting-down-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0d0ff-117">For more information, see [Shutting Down a Wrapped PST Store Provider](shutting-down-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="open-profile-section-routine"></a><span data-ttu-id="0d0ff-118">Rutina de sección de perfil abierto</span><span class="sxs-lookup"><span data-stu-id="0d0ff-118">Open Profile Section routine</span></span>

<span data-ttu-id="0d0ff-119">La función **[IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md)** abre una sección del perfil actual.</span><span class="sxs-lookup"><span data-stu-id="0d0ff-119">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function opens a section of the current profile.</span></span> <span data-ttu-id="0d0ff-120">La función requiere un tratamiento especial en la implementación del proveedor de almacén de archivos PST ajustado.</span><span class="sxs-lookup"><span data-stu-id="0d0ff-120">The function requires special handling in the wrapped PST store provider implementation.</span></span> <span data-ttu-id="0d0ff-121">Cuando `pgNSTGlobalProfileSectionGuid` se solicita, la función devuelve la sección de perfil que se almacena en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d0ff-121">When the  `pgNSTGlobalProfileSectionGuid` is requested, the function returns the profile section that is cached.</span></span> 
  
### <a name="csupportopenprofilesection-example"></a><span data-ttu-id="0d0ff-122">Ejemplo de CSupport:: OpenProfileSection ()</span><span class="sxs-lookup"><span data-stu-id="0d0ff-122">CSupport::OpenProfileSection() example</span></span>

```cpp
STDMETHODIMP CSupport::OpenProfileSection( 
    LPMAPIUID lpUid,     
    ULONG ulFlags, 
    LPPROFSECT * lppProfileObj) 
{ 
    Log(true,"CSupport::OpenProfileSection\n"); 
    if (lpUid &&  
        IsEqualMAPIUID(lpUid, (void *)&pbNSTGlobalProfileSectionGuid) &&  
        m_lpProfSect) 
    {      
        // Allow the opening of the Global Section 
        if (m_lpProfSect) 
        { 
            *lppProfileObj = m_lpProfSect; 
            (*lppProfileObj)->AddRef(); 
            return S_OK; 
        } 
    } 
    return m_pMAPISup->OpenProfileSection(lpUid, ulFlags, lppProfileObj); 
}
```

## <a name="see-also"></a><span data-ttu-id="0d0ff-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="0d0ff-123">See also</span></span>

- [<span data-ttu-id="0d0ff-124">Información sobre el proveedor de almacén de archivos PST ajustado de ejemplo</span><span class="sxs-lookup"><span data-stu-id="0d0ff-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="0d0ff-125">Instalación del proveedor de almacén de archivos PST ajustado de ejemplo</span><span class="sxs-lookup"><span data-stu-id="0d0ff-125">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="0d0ff-126">Inicializar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="0d0ff-126">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="0d0ff-127">Inicio de sesión en un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="0d0ff-127">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="0d0ff-128">Apagar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="0d0ff-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

