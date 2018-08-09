---
title: Uso de un proveedor de almacén de archivos PST ajustado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Última modificación: 03 de julio de 2012'
ms.openlocfilehash: 4a2ccbbcdd3459af6b69156d80b37695251ba8d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820948"
---
# <a name="using-a-wrapped-pst-store-provider"></a><span data-ttu-id="930bb-103">Uso de un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="930bb-103">Using a wrapped PST store provider</span></span>

<span data-ttu-id="930bb-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="930bb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="930bb-105">Para poder usar un proveedor de almacén de archivo (.pst) de carpetas personales ajustado, debe inicializar y configurar el proveedor de almacén de archivos PST ajustado.</span><span class="sxs-lookup"><span data-stu-id="930bb-105">Before you can use a wrapped Personal Folders file (PST) store provider, you must initialize and configure the wrapped PST store provider.</span></span> <span data-ttu-id="930bb-106">Después de configura el proveedor de almacén de archivos PST ajustado, debe implementar las funciones para que MAPI y la cola MAPI pueden iniciar sesión en el proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="930bb-106">After the wrapped PST store provider is configured, you must implement functions so that MAPI and the MAPI spooler can log on to the message store provider.</span></span> <span data-ttu-id="930bb-107">Para obtener más información acerca de inicializar e inicio de sesión un proveedor de almacén de archivos PST ajustado, vea [inicializar un proveedor de almacén de archivos PST ajustado](initializing-a-wrapped-pst-store-provider.md) y el [Registro en un proveedor de almacén de archivos PST ajustado](logging-on-to-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="930bb-107">For more information about initializing and logging on to a wrapped PST store provider, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md) and [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="930bb-108">La interfaz de **[IMAPISupport::IUnknown](imapisupportiunknown.md)** proporciona implementaciones para las tareas que se realizan habitualmente por mensaje los proveedores de almacén.</span><span class="sxs-lookup"><span data-stu-id="930bb-108">The **[IMAPISupport::IUnknown](imapisupportiunknown.md)** interface provides implementations for tasks that are commonly performed by message store providers.</span></span> <span data-ttu-id="930bb-109">Esta interfaz debe ser ajustada para que el proveedor de almacén de PST de ajustado de ejemplo para que funcione.</span><span class="sxs-lookup"><span data-stu-id="930bb-109">This interface must be wrapped for the Sample Wrapped PST Store Provider to work.</span></span> <span data-ttu-id="930bb-110">La función **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** requiere la implementación especial.</span><span class="sxs-lookup"><span data-stu-id="930bb-110">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function requires special implementation.</span></span> <span data-ttu-id="930bb-111">Todas las demás funciones pueden pasar sus parámetros en el objeto subyacente ajustado.</span><span class="sxs-lookup"><span data-stu-id="930bb-111">All other functions can pass their parameters to the underlying wrapped object.</span></span> 
  
<span data-ttu-id="930bb-112">En este tema, se muestra la función **IMAPISupport::OpenProfileSection** mediante el uso de un ejemplo de código desde el proveedor de almacén de archivos PST ajustado de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="930bb-112">In this topic, the **IMAPISupport::OpenProfileSection** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="930bb-113">En el ejemplo se implementa un proveedor de PST ajustado que está pensado para usarse junto con la API de replicación.</span><span class="sxs-lookup"><span data-stu-id="930bb-113">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="930bb-114">Para obtener más información sobre cómo descargar e instalar al proveedor de almacén de archivos PST ajustado de ejemplo, vea [instalar el proveedor de almacén de archivos PST ajustado de ejemplo](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="930bb-114">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="930bb-115">Para obtener más información acerca de la API de replicación, vea [Acerca de la API de replicación](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="930bb-115">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="930bb-116">Cuando termine de utilizar un proveedor de almacén de archivos PST ajustado, debe cerrar correctamente el proveedor de almacén de archivos PST ajustado.</span><span class="sxs-lookup"><span data-stu-id="930bb-116">When you finish using a wrapped PST store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="930bb-117">Para obtener más información, vea [Cerrando hacia abajo un ajustado PST proveedor de almacenamiento](shutting-down-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="930bb-117">For more information, see [Shutting Down a Wrapped PST Store Provider](shutting-down-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="open-profile-section-routine"></a><span data-ttu-id="930bb-118">Abrir rutina de sección de perfil</span><span class="sxs-lookup"><span data-stu-id="930bb-118">Open Profile Section routine</span></span>

<span data-ttu-id="930bb-119">La función **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** abre una sección del perfil actual.</span><span class="sxs-lookup"><span data-stu-id="930bb-119">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function opens a section of the current profile.</span></span> <span data-ttu-id="930bb-120">La función requiere un tratamiento especial en la implementación del proveedor de almacén de archivos PST ajustado.</span><span class="sxs-lookup"><span data-stu-id="930bb-120">The function requires special handling in the wrapped PST store provider implementation.</span></span> <span data-ttu-id="930bb-121">Cuando el `pgNSTGlobalProfileSectionGuid` se solicita, la función devuelve la sección de perfil que se almacena en caché.</span><span class="sxs-lookup"><span data-stu-id="930bb-121">When the  `pgNSTGlobalProfileSectionGuid` is requested, the function returns the profile section that is cached.</span></span> 
  
### <a name="csupportopenprofilesection-example"></a><span data-ttu-id="930bb-122">Ejemplo de CSupport::OpenProfileSection()</span><span class="sxs-lookup"><span data-stu-id="930bb-122">CSupport::OpenProfileSection() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="930bb-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="930bb-123">See also</span></span>

- [<span data-ttu-id="930bb-124">Información sobre el proveedor de almacén de archivos PST ajustado de muestra</span><span class="sxs-lookup"><span data-stu-id="930bb-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="930bb-125">Instalar la muestra de proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="930bb-125">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="930bb-126">Inicializar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="930bb-126">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="930bb-127">Iniciar sesión en un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="930bb-127">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="930bb-128">Apagar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="930bb-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

