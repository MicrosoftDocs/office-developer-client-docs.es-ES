---
title: Apagar un proveedor de almacenamiento PST ajustado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Last modified: July 02, 2012'
ms.openlocfilehash: fa918920213ee77c4d0c1d3ccc239ae7cffe81fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409947"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a><span data-ttu-id="00d7f-103">Apagar un proveedor de almacenamiento PST ajustado</span><span class="sxs-lookup"><span data-stu-id="00d7f-103">Shutting Down a Wrapped PST Store Provider</span></span>

 
  
<span data-ttu-id="00d7f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00d7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00d7f-105">Después de terminar de usar un proveedor de almacén de archivos de carpetas personales (PST) ajustado, debe cerrar correctamente el proveedor de almacenamiento PST ajustado.</span><span class="sxs-lookup"><span data-stu-id="00d7f-105">After you finish using a wrapped Personal Folders file (PST) store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="00d7f-106">Para obtener más información acerca del uso del proveedor de almacenamiento PST ajustado, vea [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="00d7f-106">For more information about using the wrapped PST store provider, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="00d7f-107">Para apagar un proveedor de almacenamiento PST ajustado, debe llamar a la **[función IMSProvider::Shutdown.](imsprovider-shutdown.md)**</span><span class="sxs-lookup"><span data-stu-id="00d7f-107">To shut down a wrapped PST store provider, you must call the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function.</span></span> <span data-ttu-id="00d7f-108">Esta función cierra el proveedor de almacenamiento PST ajustado de forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="00d7f-108">This functions closes down the wrapped PST store provider in an orderly fashion.</span></span> 
  
<span data-ttu-id="00d7f-109">En este tema, la función **IMSProvider::Shutdown** se muestra mediante un ejemplo de código del proveedor de almacén PST ajustado de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="00d7f-109">In this topic, the **IMSProvider::Shutdown** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="00d7f-110">El ejemplo implementa un proveedor de PST ajustado que está pensado para usarse junto con la API de replicación.</span><span class="sxs-lookup"><span data-stu-id="00d7f-110">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="00d7f-111">Para obtener más información acerca de cómo descargar e instalar el proveedor de la tienda PST encapsulada de muestra, consulte [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="00d7f-111">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="00d7f-112">Para obtener más información acerca de la API de replicación, vea [Acerca de la API de replicación](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="00d7f-112">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="shut-down-routine"></a><span data-ttu-id="00d7f-113">Rutina de apagado</span><span class="sxs-lookup"><span data-stu-id="00d7f-113">Shut Down Routine</span></span>

<span data-ttu-id="00d7f-114">La cola MAPI llama a la función **[IMSProvider::Shutdown](imsprovider-shutdown.md)** justo antes de liberar el proveedor del almacén PST ajustado para que el proveedor del almacén PST ajustado pueda apagarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="00d7f-114">The MAPI spooler calls the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function just before it releases the wrapped PST store provider so that the wrapped PST store provider can shut down properly.</span></span> <span data-ttu-id="00d7f-115">La función termina todos los objetos de sesión asociados con el proveedor de almacenamiento PST ajustado.</span><span class="sxs-lookup"><span data-stu-id="00d7f-115">The function terminates all session objects associated with the wrapped PST store provider.</span></span> 
  
## <a name="cmsprovidershutdown-example"></a><span data-ttu-id="00d7f-116">Ejemplo de CMSProvider::ShutDown()</span><span class="sxs-lookup"><span data-stu-id="00d7f-116">CMSProvider::ShutDown() Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="00d7f-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="00d7f-117">See also</span></span>



[<span data-ttu-id="00d7f-118">Acerca del proveedor de almacén PST ajustado de ejemplo</span><span class="sxs-lookup"><span data-stu-id="00d7f-118">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="00d7f-119">Instalación del proveedor de almacén PST ajustado de muestra</span><span class="sxs-lookup"><span data-stu-id="00d7f-119">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="00d7f-120">Inicializar un proveedor de almacenamiento PST ajustado</span><span class="sxs-lookup"><span data-stu-id="00d7f-120">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="00d7f-121">Iniciar sesión en un proveedor de almacenamiento PST ajustado</span><span class="sxs-lookup"><span data-stu-id="00d7f-121">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="00d7f-122">Uso de un proveedor de almacenamiento PST ajustado</span><span class="sxs-lookup"><span data-stu-id="00d7f-122">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)

