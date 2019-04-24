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
# <a name="shutting-down-a-wrapped-pst-store-provider"></a>Apagar un proveedor de almacén de archivos PST ajustado

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una vez que haya terminado de usar un proveedor de almacenamiento de archivos de carpetas personales ajustado (PST), debe apagar correctamente el proveedor de almacén de archivos PST ajustado. Para obtener más información acerca del uso del proveedor de almacén de archivos PST ajustado, vea [using a Conwrappedd PST Store Provider](using-a-wrapped-pst-store-provider.md).
  
Para apagar un proveedor de almacén de archivos PST ajustado, debe llamar a la función **[IMSProvider:: Shutdown](imsprovider-shutdown.md)** . Esta función cierra el proveedor de almacén de archivos PST ajustado de manera ordenada. 
  
En este tema, se muestra la función **IMSProvider:: Shutdown** mediante un ejemplo de código del proveedor de almacén de archivos PST ajustado de ejemplo. El ejemplo implementa un proveedor de archivos PST ajustado que está pensado para usarse junto con la API de replicación. Para obtener más información sobre cómo descargar e instalar el proveedor de almacén de archivos PST ajustado de ejemplo, vea [Installing the Sample wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md). Para obtener más información acerca de la API de replicación, consulte [About the replicaTION API](about-the-replication-api.md).
  
## <a name="shut-down-routine"></a>Rutina de cierre

La cola MAPI llama a la función **[IMSProvider:: Shutdown](imsprovider-shutdown.md)** inmediatamente antes de liberar el proveedor de almacén de archivos PST ajustado para que el proveedor de almacén de archivos PST ajustado pueda cerrarse correctamente. La función termina todos los objetos Session asociados con el proveedor de almacén PST ajustado. 
  
## <a name="cmsprovidershutdown-example"></a>Ejemplo de CMSProvider:: ShutDown ()

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

## <a name="see-also"></a>Vea también



[Información sobre el proveedor de almacén de archivos PST ajustado de ejemplo](about-the-sample-wrapped-pst-store-provider.md)
  
[Instalación del proveedor de almacén de archivos PST ajustado de ejemplo](installing-the-sample-wrapped-pst-store-provider.md)
  
[Inicializar un proveedor de almacén de archivos PST ajustado](initializing-a-wrapped-pst-store-provider.md)
  
[Inicio de sesión en un proveedor de almacén de archivos PST ajustado](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Usar un proveedor de almacén de archivos PST ajustado](using-a-wrapped-pst-store-provider.md)

