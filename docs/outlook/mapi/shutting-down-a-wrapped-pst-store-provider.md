---
title: Apagar un proveedor de almacén de archivos PST ajustado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Última modificación: 2012 de julio de 2002'
ms.openlocfilehash: fa918920213ee77c4d0c1d3ccc239ae7cffe81fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282785"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a><span data-ttu-id="ba71d-103">Apagar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="ba71d-103">Shutting Down a Wrapped PST Store Provider</span></span>

 
  
<span data-ttu-id="ba71d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba71d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba71d-105">Una vez que haya terminado de usar un proveedor de almacenamiento de archivos de carpetas personales ajustado (PST), debe apagar correctamente el proveedor de almacén de archivos PST ajustado.</span><span class="sxs-lookup"><span data-stu-id="ba71d-105">After you finish using a wrapped Personal Folders file (PST) store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="ba71d-106">Para obtener más información acerca del uso del proveedor de almacén de archivos PST ajustado, vea [using a Conwrappedd PST Store Provider](using-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ba71d-106">For more information about using the wrapped PST store provider, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="ba71d-107">Para apagar un proveedor de almacén de archivos PST ajustado, debe llamar a la función **[IMSProvider:: Shutdown](imsprovider-shutdown.md)** .</span><span class="sxs-lookup"><span data-stu-id="ba71d-107">To shut down a wrapped PST store provider, you must call the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function.</span></span> <span data-ttu-id="ba71d-108">Esta función cierra el proveedor de almacén de archivos PST ajustado de manera ordenada.</span><span class="sxs-lookup"><span data-stu-id="ba71d-108">This functions closes down the wrapped PST store provider in an orderly fashion.</span></span> 
  
<span data-ttu-id="ba71d-109">En este tema, se muestra la función **IMSProvider:: Shutdown** mediante un ejemplo de código del proveedor de almacén de archivos PST ajustado de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ba71d-109">In this topic, the **IMSProvider::Shutdown** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="ba71d-110">El ejemplo implementa un proveedor de archivos PST ajustado que está pensado para usarse junto con la API de replicación.</span><span class="sxs-lookup"><span data-stu-id="ba71d-110">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="ba71d-111">Para obtener más información sobre cómo descargar e instalar el proveedor de almacén de archivos PST ajustado de ejemplo, vea [Installing the Sample wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ba71d-111">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="ba71d-112">Para obtener más información acerca de la API de replicación, consulte [About the replicaTION API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="ba71d-112">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="shut-down-routine"></a><span data-ttu-id="ba71d-113">Rutina de cierre</span><span class="sxs-lookup"><span data-stu-id="ba71d-113">Shut Down Routine</span></span>

<span data-ttu-id="ba71d-114">La cola MAPI llama a la función **[IMSProvider:: Shutdown](imsprovider-shutdown.md)** inmediatamente antes de liberar el proveedor de almacén de archivos PST ajustado para que el proveedor de almacén de archivos PST ajustado pueda cerrarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="ba71d-114">The MAPI spooler calls the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function just before it releases the wrapped PST store provider so that the wrapped PST store provider can shut down properly.</span></span> <span data-ttu-id="ba71d-115">La función termina todos los objetos Session asociados con el proveedor de almacén PST ajustado.</span><span class="sxs-lookup"><span data-stu-id="ba71d-115">The function terminates all session objects associated with the wrapped PST store provider.</span></span> 
  
## <a name="cmsprovidershutdown-example"></a><span data-ttu-id="ba71d-116">Ejemplo de CMSProvider:: ShutDown ()</span><span class="sxs-lookup"><span data-stu-id="ba71d-116">CMSProvider::ShutDown() Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="ba71d-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba71d-117">See also</span></span>



[<span data-ttu-id="ba71d-118">Información sobre el proveedor de almacén de archivos PST ajustado de ejemplo</span><span class="sxs-lookup"><span data-stu-id="ba71d-118">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="ba71d-119">Instalación del proveedor de almacén de archivos PST ajustado de ejemplo</span><span class="sxs-lookup"><span data-stu-id="ba71d-119">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="ba71d-120">Inicializar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="ba71d-120">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="ba71d-121">Inicio de sesión en un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="ba71d-121">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="ba71d-122">Usar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="ba71d-122">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)

