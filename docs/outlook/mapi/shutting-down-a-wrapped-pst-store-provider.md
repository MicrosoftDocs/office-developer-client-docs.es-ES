---
title: Apagar un proveedor de almacén de PST ajustado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Última modificación: 2 de julio de 2012'
ms.openlocfilehash: fa918920213ee77c4d0c1d3ccc239ae7cffe81fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409947"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a>Apagar un proveedor de almacén de PST ajustado

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una vez que termine de usar un proveedor de almacén de archivos de carpetas personales (PST) ajustado, debe apagar correctamente el proveedor de almacén de ARCHIVOS PST ajustado. Para obtener más información acerca del uso del proveedor de almacenamiento de PST ajustado, vea [El uso de un proveedor de almacén de PST ajustado.](using-a-wrapped-pst-store-provider.md)
  
Para apagar un proveedor de almacén de PST ajustado, debe llamar a la **[función IMSProvider::Shutdown.](imsprovider-shutdown.md)** Esta función cierra el proveedor del almacén de PST ajustado de forma ordenada. 
  
En este tema, la función **IMSProvider::Shutdown** se muestra mediante un ejemplo de código del proveedor de almacén pst ajustado de ejemplo. El ejemplo implementa un proveedor de PST ajustado que está pensado para usarse junto con la API de replicación. Para obtener más información acerca de cómo descargar e instalar el proveedor de almacén de ARCHIVOS PST ajustados de ejemplo, consulte Instalación del proveedor de almacén pst ajustado [de ejemplo.](installing-the-sample-wrapped-pst-store-provider.md) Para obtener más información acerca de la API de replicación, vea [Acerca de la API de replicación.](about-the-replication-api.md)
  
## <a name="shut-down-routine"></a>Rutina de cierre

La cola MAPI llama a la función **[IMSProvider::Shutdown](imsprovider-shutdown.md)** justo antes de liberar el proveedor de almacén de PST ajustado para que el proveedor de almacenamiento de PST ajustado pueda apagarse correctamente. La función finaliza todos los objetos de sesión asociados con el proveedor de almacén de PST ajustado. 
  
## <a name="cmsprovidershutdown-example"></a>Ejemplo de CMSProvider::ShutDown()

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

## <a name="see-also"></a>Consulte también



[Acerca del proveedor de almacenamiento PST ajustado de ejemplo](about-the-sample-wrapped-pst-store-provider.md)
  
[Instalación del proveedor de almacén pst ajustado de ejemplo](installing-the-sample-wrapped-pst-store-provider.md)
  
[Inicialización de un proveedor de almacén de PST ajustado](initializing-a-wrapped-pst-store-provider.md)
  
[Inicio de sesión en un proveedor de almacén de PST ajustado](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Uso de un proveedor de almacén de PST ajustado](using-a-wrapped-pst-store-provider.md)

