---
title: Usar un proveedor de almacén de archivos PST ajustado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: b7c651044ab7f4cad7032db69e157c9a3589bde9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420825"
---
# <a name="using-a-wrapped-pst-store-provider"></a>Usar un proveedor de almacén de archivos PST ajustado

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para poder usar un proveedor de almacén de archivos de carpetas personales ajustado (PST), debe inicializar y configurar el proveedor de almacenamiento PST ajustado. Una vez configurado el proveedor de almacenamiento PST ajustado, debe implementar funciones para que MAPI y la cola MAPI puedan iniciar sesión en el proveedor del almacén de mensajes. Para obtener más información sobre la inicialización y el inicio de sesión en un proveedor de almacenamiento PST ajustado, vea [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md) y [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).
  
La **[interfaz IMAPISupport::IUnknown](imapisupportiunknown.md)** proporciona implementaciones para las tareas que normalmente realizan los proveedores de almacenes de mensajes. Esta interfaz debe ajustarse para que funcione el proveedor de almacén PST ajustado de muestra. La **[función IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** requiere una implementación especial. Todas las demás funciones pueden pasar sus parámetros al objeto ajustado subyacente. 
  
En este tema, la función **IMAPISupport::OpenProfileSection** se muestra mediante un ejemplo de código del proveedor de almacén PST ajustado de ejemplo. El ejemplo implementa un proveedor de PST ajustado que está pensado para usarse junto con la API de replicación. Para obtener más información acerca de cómo descargar e instalar el proveedor de la tienda PST encapsulada de muestra, consulte [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md). Para obtener más información acerca de la API de replicación, vea [Acerca de la API de replicación](about-the-replication-api.md).
  
Cuando termine de usar un proveedor de almacenamiento PST ajustado, debe apagar correctamente el proveedor de almacenamiento PST ajustado. Para obtener más información, vea [Shutting Down a Wrapped PST Store Provider](shutting-down-a-wrapped-pst-store-provider.md).
  
## <a name="open-profile-section-routine"></a>Rutina abrir sección de perfil

La **[función IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** abre una sección del perfil actual. La función requiere un control especial en la implementación del proveedor del almacén PST ajustado. Cuando se  `pgNSTGlobalProfileSectionGuid` solicita, la función devuelve la sección de perfil que se almacena en caché. 
  
### <a name="csupportopenprofilesection-example"></a>Ejemplo CSupport::OpenProfileSection()

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

## <a name="see-also"></a>Vea también

- [Acerca del proveedor de almacén PST ajustado de ejemplo](about-the-sample-wrapped-pst-store-provider.md)
- [Instalación del proveedor de almacén PST ajustado de muestra](installing-the-sample-wrapped-pst-store-provider.md)
- [Inicializar un proveedor de almacenamiento PST ajustado](initializing-a-wrapped-pst-store-provider.md)
- [Iniciar sesión en un proveedor de almacenamiento PST ajustado](logging-on-to-a-wrapped-pst-store-provider.md)
- [Apagar un proveedor de almacenamiento PST ajustado](shutting-down-a-wrapped-pst-store-provider.md)

