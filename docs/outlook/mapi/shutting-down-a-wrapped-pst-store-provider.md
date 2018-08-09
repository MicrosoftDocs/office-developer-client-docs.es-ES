---
title: Apagar un proveedor de almacén de archivos PST ajustado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Última modificación: 02 de julio de 2012'
ms.openlocfilehash: 5c8ad7443b0c1aa05f48284e4b09859ab53dd2c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820664"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a><span data-ttu-id="6f1e9-103">Apagar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="6f1e9-103">Shutting Down a Wrapped PST Store Provider</span></span>

 
  
<span data-ttu-id="6f1e9-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6f1e9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6f1e9-105">Cuando termine de usar un proveedor de almacén de archivo (.pst) de carpetas personales ajustado, debe cerrar correctamente el proveedor de almacén de archivos PST ajustado.</span><span class="sxs-lookup"><span data-stu-id="6f1e9-105">After you finish using a wrapped Personal Folders file (PST) store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="6f1e9-106">Para obtener más información acerca de cómo utilizar el proveedor de almacén de archivos PST ajustado, vea [uso de un proveedor de almacén de archivos PST ajustado](using-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6f1e9-106">For more information about using the wrapped PST store provider, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="6f1e9-107">Para cerrar un proveedor de almacén de archivos PST ajustado, debe llamar a la función **[IMSProvider::Shutdown](imsprovider-shutdown.md)** .</span><span class="sxs-lookup"><span data-stu-id="6f1e9-107">To shut down a wrapped PST store provider, you must call the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function.</span></span> <span data-ttu-id="6f1e9-108">Esta funciones se cierra el proveedor de almacenamiento de archivos PST ajustado de forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="6f1e9-108">This functions closes down the wrapped PST store provider in an orderly fashion.</span></span> 
  
<span data-ttu-id="6f1e9-109">En este tema, se muestra la función **IMSProvider::Shutdown** mediante el uso de un ejemplo de código desde el proveedor de almacén de archivos PST ajustado de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="6f1e9-109">In this topic, the **IMSProvider::Shutdown** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="6f1e9-110">En el ejemplo se implementa un proveedor de PST ajustado que está pensado para usarse junto con la API de replicación.</span><span class="sxs-lookup"><span data-stu-id="6f1e9-110">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="6f1e9-111">Para obtener más información sobre cómo descargar e instalar al proveedor de almacén de archivos PST ajustado de ejemplo, vea [instalar el proveedor de almacén de archivos PST ajustado de ejemplo](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6f1e9-111">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="6f1e9-112">Para obtener más información acerca de la API de replicación, vea [Acerca de la API de replicación](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="6f1e9-112">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="shut-down-routine"></a><span data-ttu-id="6f1e9-113">Apague la rutina</span><span class="sxs-lookup"><span data-stu-id="6f1e9-113">Shut Down Routine</span></span>

<span data-ttu-id="6f1e9-114">La cola MAPI llama a la función **[IMSProvider::Shutdown](imsprovider-shutdown.md)** justo antes de que libera el proveedor de almacén de archivos PST ajustado para que el proveedor de almacén de archivos PST ajustado puede apagar correctamente.</span><span class="sxs-lookup"><span data-stu-id="6f1e9-114">The MAPI spooler calls the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function just before it releases the wrapped PST store provider so that the wrapped PST store provider can shut down properly.</span></span> <span data-ttu-id="6f1e9-115">La función termina todos los objetos de sesión asociados con el proveedor de almacén de archivos PST ajustado.</span><span class="sxs-lookup"><span data-stu-id="6f1e9-115">The function terminates all session objects associated with the wrapped PST store provider.</span></span> 
  
## <a name="cmsprovidershutdown-example"></a><span data-ttu-id="6f1e9-116">Ejemplo de CMSProvider::ShutDown()</span><span class="sxs-lookup"><span data-stu-id="6f1e9-116">CMSProvider::ShutDown() Example</span></span>

```cpp
STDMETHODIMP CMSProvider::Shutdown(ULONG * pulFlags) 
{ 
    HRESULT hRes = S_OK; 
    Log(true,"CMSProvider::Shutdown\n"); 
    hRes =m_pPSTMS->Shutdown(pulFlags); 
    Log(true,"CMSProvider::Shutdown returned: 0x%08X\n", hRes); 
    return hRes ;  
}
```

## <a name="see-also"></a><span data-ttu-id="6f1e9-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f1e9-117">See also</span></span>



[<span data-ttu-id="6f1e9-118">Información sobre el proveedor de almacén de archivos PST ajustado de muestra</span><span class="sxs-lookup"><span data-stu-id="6f1e9-118">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="6f1e9-119">Instalar la muestra de proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="6f1e9-119">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="6f1e9-120">Inicializar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="6f1e9-120">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="6f1e9-121">Iniciar sesión en un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="6f1e9-121">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="6f1e9-122">Usar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="6f1e9-122">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)

